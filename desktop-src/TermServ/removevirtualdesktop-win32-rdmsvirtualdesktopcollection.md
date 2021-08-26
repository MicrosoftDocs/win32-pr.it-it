---
title: Metodo RemoveVirtualDesktop della Win32_RDMSVirtualDesktopCollection classe
description: Rimuove un desktop virtuale dall'insieme di desktop virtuali.
ms.assetid: 287ebbb2-86db-4b4a-8dbb-ac5472789e72
ms.tgt_platform: multiple
keywords:
- Metodo RemoveVirtualDesktop Servizi Desktop remoto
- Metodo RemoveVirtualDesktop Servizi Desktop remoto , Win32_RDMSVirtualDesktopCollection classe
- Win32_RDMSVirtualDesktopCollection classe Servizi Desktop remoto , metodo RemoveVirtualDesktop
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.RemoveVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3deefa38d7c7fcfc3f7942eb809b2ca14e96ea14ee4f2e014cdf3e0069a6ab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009181"
---
# <a name="removevirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo RemoveVirtualDesktop della classe \_ WIN32 RDMSVirtualDesktopCollection

Rimuove un desktop virtuale dall'insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VMName* \[ Pollici\]
</dt> <dd>

Nome della macchina virtuale che ospita il desktop virtuale.

</dd> </dl>

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

 

 





