---
title: Metodo GetVirtualDesktopDetails della classe Win32_RDMSVirtualDesktop
description: Recupera le informazioni aggiuntive sul desktop virtuale.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetVirtualDesktopDetails
- Metodo GetVirtualDesktopDetails Servizi Desktop remoto, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Servizi Desktop remoto, metodo GetVirtualDesktopDetails
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477446"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a>Metodo GetVirtualDesktopDetails della \_ classe RDMSVirtualDesktop Win32

Recupera le informazioni aggiuntive sul desktop virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RAMSizeInMB* \[ out\]
</dt> <dd>

Riceve la quantità di RAM assegnata al desktop virtuale, in byte.

</dd> <dt>

*RemoteFXEnabled* \[ out\]
</dt> <dd>

Riceve un valore che indica se RemoteFX è abilitato sul desktop virtuale. **True** se RemoteFX è abilitato; in caso contrario, **false**.

</dd> <dt>

*OSVersion* \[ out\]
</dt> <dd>

Riceve la versione del sistema operativo del desktop virtuale.

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

[**\_RDMSVirtualDesktop Win32**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





