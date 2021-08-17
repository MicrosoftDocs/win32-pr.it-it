---
title: Metodo GetVirtualDesktopDetails della Win32_RDMSVirtualDesktop classe
description: Recupera le informazioni aggiuntive sul desktop virtuale.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- Metodo GetVirtualDesktopDetails Servizi Desktop remoto
- Metodo GetVirtualDesktopDetails Servizi Desktop remoto , Win32_RDMSVirtualDesktop classe
- Win32_RDMSVirtualDesktop classe Servizi Desktop remoto , metodo GetVirtualDesktopDetails
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
ms.openlocfilehash: b6ca1b552147623822ae007ca17abf8e4eaebfb149f5e80ac4760719f1ef7168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059489"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a>Metodo GetVirtualDesktopDetails della classe \_ WIN32 RDMSVirtualDesktop

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

*RAMSizeInMB* \[ Cambio\]
</dt> <dd>

Riceve la quantità di RAM assegnata al desktop virtuale, in byte.

</dd> <dt>

*RemoteFXEnabled* \[ Cambio\]
</dt> <dd>

Riceve un valore che indica se RemoteFX è abilitato nel desktop virtuale. **TRUE** se RemoteFX è abilitato; in caso contrario, **FALSE.**

</dd> <dt>

*OSVersion* \[ Cambio\]
</dt> <dd>

Riceve la versione del sistema operativo del desktop virtuale.

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

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





