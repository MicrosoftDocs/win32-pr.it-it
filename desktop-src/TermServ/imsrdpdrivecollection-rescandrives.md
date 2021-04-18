---
title: Metodo IMsRdpDriveCollection RescanDrives
description: Aggiorna l'elenco di oggetti nella raccolta. | Metodo IMsRdpDriveCollection RescanDrives
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RescanDrives
- Metodo RescanDrives Servizi Desktop remoto, interfaccia IMsRdpDriveCollection
- Interfaccia IMsRdpDriveCollection Servizi Desktop remoto, metodo RescanDrives
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7488187e44caeaedb7c73b01ff8a3711e20dcdd1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321237"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a>Metodo IMsRdpDriveCollection:: RescanDrives

Aggiorna l'elenco di oggetti nella raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vboolDynRedir* \[ in\]
</dt> <dd>

Stato di reindirizzamento predefinito che verrà applicato alle unità o ai dispositivi appena individuati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, viene restituito **S \_ OK** . Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection è definito come 7ff17599-da2c-4677-Ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





