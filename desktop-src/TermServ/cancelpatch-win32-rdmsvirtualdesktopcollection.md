---
title: Metodo CancelPatch della classe Win32_RDMSVirtualDesktopCollection
description: Annulla un processo di provisioning degli aggiornamenti software per le macchine virtuali in una raccolta di desktop virtuali.
ms.assetid: fb0d6831-5c69-4017-b725-1a5038ad69f5
ms.tgt_platform: multiple
keywords:
- Metodo CancelPatch Servizi Desktop remoto
- Il metodo CancelPatch Servizi Desktop remoto , Win32_RDMSVirtualDesktopCollection classe
- Win32_RDMSVirtualDesktopCollection classe Servizi Desktop remoto , metodo CancelPatch
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.CancelPatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e355051fd1ef9ceca2925ab3e499824dabe605670ee9e732a08809e474f5ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131330"
---
# <a name="cancelpatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo CancelPatch della classe \_ WIN32 RDMSVirtualDesktopCollection

Annulla un processo di provisioning degli aggiornamenti software per le macchine virtuali in una raccolta di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 CancelPatch();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Root \\ CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





