---
title: Metodo AddVirtualDesktop della classe Win32_RDMSVirtualDesktopCollection
description: Aggiunge un desktop virtuale all'insieme di desktop virtuali.
ms.assetid: 31a3aa28-6e5d-4f8a-81ff-ab011f568b6a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddVirtualDesktop
- Metodo AddVirtualDesktop Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo AddVirtualDesktop
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
ms.openlocfilehash: 4858f99f2ea4793fe0d83d06a0aaa429b7aa8f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517499"
---
# <a name="addvirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo AddVirtualDesktop della \_ classe RDMSVirtualDesktopCollection Win32

Aggiunge un desktop virtuale all'insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VMName* \[ in\]
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
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





