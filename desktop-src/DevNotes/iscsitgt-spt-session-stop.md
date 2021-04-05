---
description: Usato con il \_ \_ codice di controllo ioctl SCSI miniport IOCTL e CTLCODE \_ ISCSITGT \_ SPT \_ Session \_ End (0x101) per arrestare una sessione.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: Struttura ISCSITGT_SPT_SESSION_STOP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "103886064"
---
# <a name="iscsitgt_spt_session_stop-structure"></a>\_Struttura di \_ arresto della sessione ISCSITGT SPT \_

\[La struttura seguente è disponibile per l'uso in Windows Server 2012 R2. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Usato con il codice di controllo IOCTL [**\_ SCSI \_ Miniport**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL e CTLCODE \_ ISCSITGT \_ SPT \_ Session \_ End (0x101) per arrestare una sessione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a>Members

<dl> <dt>

**Intestazione**
</dt> <dd>

Intestazione obbligatoria.

</dd> <dt>

**ITNexusHandle**
</dt> <dd>

Handle opaco che rappresenta una sessione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/> |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                               |
| Fine del supporto server<br/>    | Windows Server 2012 R2<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Pass-through di destinazione iSCSI](/powershell/module/iscsi)
</dt> <dt>

[**\_controllo di io SRB \_**](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
