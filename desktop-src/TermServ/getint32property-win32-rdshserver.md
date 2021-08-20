---
title: Metodo GetInt32Property della classe Win32_RDSHServer (Microsoft.diagnostics.appanalysis.h)
description: Recupera il valore di una proprietà integer di un oggetto \_ RDSHServer Win32.
ms.assetid: 4601e9cb-927b-4af8-a12b-09a8ca44c2f7
ms.tgt_platform: multiple
keywords:
- Metodo GetInt32Property Servizi Desktop remoto
- Metodo GetInt32Property Servizi Desktop remoto , Win32_RDSHServer classe
- Win32_RDSHServer classe Servizi Desktop remoto metodo , GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba9114ca22a1052161000fcb05f38622ab9d210ec02b14715dad1bb85ce1365e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130672"
---
# <a name="getint32property-method-of-the-win32_rdshserver-class"></a>Metodo GetInt32Property della classe RDSHServer Win32 \_

Recupera il valore di una proprietà integer di un [**oggetto \_ RDSHServer Win32.**](win32-rdshserver.md)

## <a name="syntax"></a>Sintassi


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Chiave che identifica la proprietà da recuperare.

</dd> <dt>

*Valore* \[ Cambio\]
</dt> <dd>

Riceve il valore della proprietà recuperata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                                      |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                                 |
| Spazio dei nomi<br/>                | Rdms \\ CIMv2 \\ radice<br/>                                                                                   |
| Intestazione<br/>                   | <dl> <dt>Microsoft.diagnostics.appanalysis.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 





