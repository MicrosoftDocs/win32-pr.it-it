---
title: Metodo IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Riceve una notifica che segnala che il supporto è stato espulso dall'unità. | Metodo IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- Metodo OnMediaEject Virtual PC
- Metodo OnMediaEject Virtual PC, interfaccia IVMDVDDriveEvents
- Interfaccia IVMDVDDriveEvents Virtual PC, metodo OnMediaEject
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b66091dcc6cc5ee28ab6e0cb3d58e3e647e41cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886095"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a>Metodo IVMDVDDriveEvents:: OnMediaEject

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Riceve una notifica che segnala che il supporto è stato espulso dall'unità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mediaPath* \[ in\]
</dt> <dd>

Lettera o percorso dell'unità host nell'immagine ISO.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando viene espulso il supporto (un'immagine ISO o un disco in un'unità host). Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento vmDVDDriveEvent oneject originato da [**IVMDVDDrive**](ivmdvddrive.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents è definito come c2a7d8e9-E76C-4EB8-94f7-71a5122d249b<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

