---
title: Metodo GetInt32Property della Win32_RDSHCollection classe (Microsoft.diagnostics.appanalysis.h)
description: Recupera un valore della proprietà Integer di un oggetto \_ RDSHCollection Win32.
ms.assetid: ab68f357-057d-4a36-ae39-f47198768a49
ms.tgt_platform: multiple
keywords:
- Metodo GetInt32Property Servizi Desktop remoto
- Metodo GetInt32Property Servizi Desktop remoto , Win32_RDSHCollection classe
- Win32_RDSHCollection classe Servizi Desktop remoto metodo , GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61fb64c55a0b361ec4f3ca8528247f3884684b3321251c81594c3161c83a8c7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130716"
---
# <a name="getint32property-method-of-the-win32_rdshcollection-class"></a>Metodo GetInt32Property della classe RDSHCollection Win32 \_

Recupera un valore della proprietà Integer di un [**oggetto \_ RDSHCollection Win32.**](win32-rdshcollection.md)

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

Riceve il valore della proprietà recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                                      |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                                 |
| Spazio dei nomi<br/>                | Root \\ CIMv2 \\ rdms<br/>                                                                                   |
| Intestazione<br/>                   | <dl> <dt>Microsoft.diagnostics.appanalysis.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





