---
title: Metodo IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces.h)
description: Riceve una notifica che indica che i supporti sono stati inseriti nell'unità. | Metodo IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces.h)
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- Metodo OnMediaInsert Virtual PC
- Metodo OnMediaInsert Virtual PC, interfaccia IVMDVDDriveEvents
- Interfaccia IVMDVDDriveEvents Virtual PC, metodo OnMediaInsert
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b19beabfcc4cab182af850d27d3d45ea565b266e8bcaa8fa2488aa145f43fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595735"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a>Metodo IVMDVDDriveEvents::OnMediaInsert

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Riceve una notifica che indica che i supporti sono stati inseriti nell'unità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnMediaInsert(
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

Questo metodo viene chiamato quando viene inserito un supporto (un'immagine ISO o un disco in un'unità host). Il programma client deve implementare questo metodo di interfaccia per ricevere la notifica dell'evento OnInsert vmDVDDriveEvent \_ originato da [**IVMDVDDrive.**](ivmdvddrive.md)

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

 

