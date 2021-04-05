---
title: Metodo IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Riceve una notifica che segnala che il supporto è stato espulso dall'unità. | Metodo IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
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
ms.openlocfilehash: fd640f7b8eb143eba4f3b19e984792f2b6779ad6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886255"
---
# <a name="ivmfloppydriveeventsonmediaeject-method"></a>Metodo IVMFloppyDriveEvents:: OnMediaEject

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

Lettera o percorso dell'unità host nell'immagine floppy.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando viene espulso il supporto (un'immagine del disco floppy o un disco floppy in un'unità host). Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento vmFloppyDriveEvent OnMediaEject originato da [**IVMFloppyDrive**](ivmfloppydrive.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents è definito come a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

