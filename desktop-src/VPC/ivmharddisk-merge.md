---
title: Metodo Merge IVMHardDisk (VPCCOMInterfaces. h)
description: Unisce un disco rigido virtuale differenze con l'immagine del disco padre.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Metodo Merge Virtual PC
- Metodo Merge Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, metodo Merge
topic_type:
- apiref
api_name:
- IVMHardDisk.Merge
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5e4b32cb1df2f754463cee7f8275b00f86513b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964414"
---
# <a name="ivmharddiskmerge-method"></a>Metodo IVMHardDisk:: merge

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Unisce un disco rigido virtuale differenze con l'immagine del disco padre.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia del completamento del processo di Unione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'operazione è stata completata.<br/>                                                                                                                                                                                          |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                      | Il parametro è **null**.<br/>                                                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (violazione della condivisione degli errori \_ \_ )**</dt> <dt>0x80070020</dt> </dl> | L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) è in uso o l'elemento padre di questa immagine del disco rigido virtuale è in uso. In alternativa, è possibile che le immagini del disco rigido facciano parte di uno stato salvato.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ tipo di \_ immagine \_ HD errato**</dt> <dt>0xA004067B</dt> </dl>                   | L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) deve essere un'immagine del disco differenze.<br/>                                                                                            |
| <dl> <dt>**Macchina virtuale \_ E \_ file \_ \_**</dt> di sola lettura <dt>0xA004067A</dt> </dl>                         | L'elemento padre dell'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) è contrassegnato come di sola lettura.<br/>                                                                                             |
| <dl> <dt>**Macchina virtuale \_ \_Percorso padre \_ E \_ non \_ trovato**</dt> <dt>0xA0040677</dt> </dl>                 | L'elemento padre del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) non esiste.<br/>                                                                                                       |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ chiusura \_ dell'app**</dt> <dt>0xA0040209</dt> </dl>                      | Non è possibile eseguire il merge dell'immagine del disco rigido virtuale perché è in corso la chiusura dell'applicazione.<br/>                                                                                                                                 |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                              | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

