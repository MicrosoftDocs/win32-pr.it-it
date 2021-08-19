---
title: Metodo IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces.h)
description: Riceve la notifica che il supporto è stato espulso dall'unità. | Metodo IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces.h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- Metodo OnMediaEject Virtual PC
- Metodo OnMediaEject Virtual PC , interfaccia IVMDVDDriveEvents
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
ms.openlocfilehash: 6e2fbf9ffe589597e1baab7c0b503cf94384cfa540749cfe49e083286f743370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753752"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a>Metodo IVMDVDDriveEvents::OnMediaEject

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Riceve la notifica che il supporto è stato espulso dall'unità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mediaPath* \[ Pollici\]
</dt> <dd>

Lettera di unità host, o percorso, dell'immagine ISO.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando viene espulso un supporto (un'immagine ISO o un disco in un'unità host). Il programma client deve implementare questo metodo di interfaccia per ricevere la notifica dell'evento vmDVDDriveEvent OnEject che ha origine \_ da [**IVMDVDDrive.**](ivmdvddrive.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents è definito come c2a7d8e9-e76c-4eb8-94f7-71a5122d249b<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

