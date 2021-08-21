---
title: Metodo AddVirtualDesktop della classe Win32_RDMSVirtualDesktopCollection
description: Aggiunge un desktop virtuale alla raccolta di desktop virtuali.
ms.assetid: 31a3aa28-6e5d-4f8a-81ff-ab011f568b6a
ms.tgt_platform: multiple
keywords:
- Metodo AddVirtualDesktop Servizi Desktop remoto
- Metodo AddVirtualDesktop Servizi Desktop remoto , Win32_RDMSVirtualDesktopCollection classe
- Win32_RDMSVirtualDesktopCollection classe Servizi Desktop remoto , metodo AddVirtualDesktop
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.AddVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd677c475fd64e8b847540a312568e551b3c7c3f1ad1887082637b29c025abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131310"
---
# <a name="addvirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo AddVirtualDesktop della classe \_ RDMSVirtualDesktopCollection Win32

Aggiunge un desktop virtuale alla raccolta di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddVirtualDesktop(
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

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Rdms \\ CIMv2 \\ radice<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





