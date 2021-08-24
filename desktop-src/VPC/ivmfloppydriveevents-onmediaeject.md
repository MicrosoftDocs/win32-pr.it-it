---
title: Metodo OnMediaEject IVMFloppyDriveEvents (VPCCOMInterfaces.h)
description: Riceve la notifica che il supporto è stato espulso dall'unità. | Metodo OnMediaEject IVMFloppyDriveEvents (VPCCOMInterfaces.h)
ms.assetid: 3e9c0b5d-8fec-4f34-93d2-c5975403798b
keywords:
- Metodo OnMediaEject Virtual PC
- Metodo OnMediaEject Virtual PC, interfaccia IVMFloppyDriveEvents
- Interfaccia IVMFloppyDriveEvents Virtual PC, metodo OnMediaEject
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e624dcbf028caf58a2f50109789e5f89cd34d1d70c4679333b8b742c3b071ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653601"
---
# <a name="ivmfloppydriveeventsonmediaeject-method"></a>Metodo IVMFloppyDriveEvents::OnMediaEject

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

Lettera dell'unità host, o percorso, dell'immagine floppy.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando viene espulso un supporto (un'immagine di disco floppy o un disco floppy in un'unità host). Il programma client deve implementare questo metodo di interfaccia per ricevere la notifica dell'evento vmFloppyDriveEvent \_ OnMediaEject proveniente da [**IVMFloppyDrive.**](ivmfloppydrive.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents è definito come a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

