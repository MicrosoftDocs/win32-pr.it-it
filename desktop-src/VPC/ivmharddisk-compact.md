---
title: Metodo IVMHardDisk Compact (VPCCOMInterfaces.h)
description: Compatta un'immagine del disco rigido virtuale a espansione dinamica.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Metodo Compact Virtual PC
- Metodo Compact Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, metodo Compact
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d2ae6c8bcb4237f98c8bcb47089294b202e3e9c45e51351c9818a08e2a295ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472166"
---
# <a name="ivmharddiskcompact-method"></a>Metodo IVMHardDisk::Compact

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Compatta un'immagine del disco rigido virtuale a espansione dinamica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*compactTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia del completamento del processo di compattazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                              | Descrizione                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'operazione è stata completata.<br/>                                                                                                        |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                              | Si è verificato un errore imprevisto.<br/>                                                                                                    |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                      | Il parametro è **NULL.**<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ SHARING \_ VIOLATION)**</dt> <dt>0X80070020</dt> </dl> | L'immagine del disco rigido virtuale a cui fa [**riferimento questo oggetto IVMHardDisk**](ivmharddisk.md) è in uso.<br/>                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>         | Il volume host non dispone di spazio sufficiente per creare un file temporaneo necessario per la compattazione di questa immagine del disco rigido virtuale.<br/>     |
| <dl> <dt>**Macchina virtuale \_ E \_ APP \_ SHUTTING \_ DOWN**</dt> <dt>0xA0040209</dt> </dl>                      | L'immagine del disco rigido virtuale non può essere compattata perché l'applicazione è in fase di arresto.<br/>                                            |
| <dl> <dt>**Macchina virtuale \_ E \_ FILE \_ READ \_ ONLY**</dt> <dt>0xA004067A</dt> </dl>                         | L'immagine del disco rigido virtuale a cui fa [**riferimento questo oggetto IVMHardDisk**](ivmharddisk.md) è contrassegnata come di sola lettura.<br/>                     |
| <dl> <dt>**Macchina virtuale \_ E \_ TIPO DI IMMAGINE HD \_ \_ \_ ERRATO**</dt> <dt>0XA004067B</dt> </dl>                   | L'immagine del disco rigido virtuale a cui fa riferimento questo [**oggetto IVMHardDisk**](ivmharddisk.md) deve essere un **tipo di immagine vmDiskTypeDynamic.**<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ FILE HD NON \_ \_ VALIDO**</dt> <dt>0xA0040682</dt> </dl>                        | L'immagine del disco rigido virtuale a cui fa riferimento questo [**oggetto IVMHardDisk**](ivmharddisk.md) non sembra essere un'immagine valida.<br/>          |



 

## <a name="remarks"></a>Commenti

Per compattare un'immagine del disco rigido a espansione dinamica, è prima necessario azzerare lo spazio disponibile nell'immagine del disco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

