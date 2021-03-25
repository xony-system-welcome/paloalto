#### Downgrade
Check the previous PAN-OS\
```> debug swm status```

Downgrade to previous PAN-OS, will not remove and change any thing and setting\
```> debug swm revert```

Reboot system for previous version\
```> request restart system```

#### Rollback
Auto boot PA maint mode\
```> debug system maintenance-mode```

Select run mode\
```PANOS (Maint)```

Continue\
```Continue```

Select Recovery Rool\
```Factory Reset```

Advanced Password\
```MA1NT```

Select image, then factory reset\
```Panos-x.x.x```
```Factory Reset```

Rebook run system\
```Rebook```
