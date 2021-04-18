---
title: Metodo IVMFloppyDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
description: Riceve la notifica che i supporti sono stati inseriti nell'unità. | Metodo IVMFloppyDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- Metodo OnMediaInsert Virtual PC
- Metodo OnMediaInsert Virtual PC, interfaccia IVMFloppyDriveEvents
- Interfaccia IVMFloppyDriveEvents Virtual PC, metodo OnMediaInsert
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d607a2f63836ca1cb151e602b2d3b2021f4e3913
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321984"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a>Metodo IVMFloppyDriveEvents:: OnMediaInsert

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Riceve la notifica che i supporti sono stati inseriti nell'unità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnMediaInsert(
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

Questo metodo viene chiamato quando viene inserito un supporto (un'immagine del disco floppy o un disco floppy in un'unità host). Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento vmFloppyDriveEvent OnMediaInsert originato da [**IVMFloppyDrive**](ivmfloppydrive.md).

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

 

