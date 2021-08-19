---
title: Metodo Merge IVMHardDisk (VPCCOMInterfaces.h)
description: Unisce un disco rigido virtuale differenze con l'immagine del disco padre.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Metodo merge Virtual PC
- Metodo merge Virtual PC, interfaccia IVMHardDisk
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
ms.openlocfilehash: 5b1683b5a44d8418dc247dddcfde52b369c293484e5c3b19c139fe25521ac6c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998941"
---
# <a name="ivmharddiskmerge-method"></a>Metodo IVMHardDisk::Merge

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia del completamento del processo di unione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'operazione è stata completata.<br/>                                                                                                                                                                                          |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                      | Il parametro è **NULL.**<br/>                                                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ SHARING \_ VIOLATION)**</dt> <dt>0X80070020</dt> </dl> | L'immagine del disco rigido virtuale a cui fa riferimento questo [**oggetto IVMHardDisk**](ivmharddisk.md) è in uso o l'elemento padre di questa immagine del disco rigido virtuale è in uso. In caso contrario, queste immagini del disco rigido potrebbero far parte di uno stato salvato.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ TIPO DI IMMAGINE HD \_ \_ \_ 0XA004067B**</dt> <dt></dt> </dl>                   | L'immagine del disco rigido virtuale a cui fa riferimento [**questo oggetto IVMHardDisk**](ivmharddisk.md) deve essere un'immagine disco differenze.<br/>                                                                                            |
| <dl> <dt>**Macchina virtuale \_ E \_ FILE \_ DI \_ SOLA**</dt> <dt>lettura 0xA004067A</dt> </dl>                         | L'elemento padre dell'immagine del disco rigido virtuale a cui fa riferimento [**questo oggetto IVMHardDisk**](ivmharddisk.md) è contrassegnato come di sola lettura.<br/>                                                                                             |
| <dl> <dt>**Macchina virtuale \_ E \_ PERCORSO PADRE NON TROVATO \_ \_ \_ 0XA0040677**</dt> <dt></dt> </dl>                 | L'elemento padre del disco rigido virtuale a cui fa riferimento questo [**oggetto IVMHardDisk**](ivmharddisk.md) non esiste.<br/>                                                                                                       |
| <dl> <dt>**Macchina virtuale \_ E \_ ARRESTO \_ DELL'APP \_ 0XA0040209**</dt> <dt></dt> </dl>                      | Impossibile unire l'immagine del disco rigido virtuale perché l'applicazione è in fase di arresto.<br/>                                                                                                                                 |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDisk è definito come \_ ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

