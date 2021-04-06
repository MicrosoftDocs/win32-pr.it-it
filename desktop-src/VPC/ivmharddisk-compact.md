---
title: Metodo Compact IVMHardDisk (VPCCOMInterfaces. h)
description: Compatta un'immagine del disco rigido virtuale ad espansione dinamica.
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
ms.openlocfilehash: 51b28b47709fdf956b679a4f16c50adde4a1b335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743247"
---
# <a name="ivmharddiskcompact-method"></a>Metodo IVMHardDisk:: Compact

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Compatta un'immagine del disco rigido virtuale ad espansione dinamica.

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

Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia del processo di compattazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                              | Descrizione                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'operazione è stata completata.<br/>                                                                                                        |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                              | Si è verificato un errore imprevisto.<br/>                                                                                                    |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                      | Il parametro è **null**.<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (violazione della condivisione degli errori \_ \_ )**</dt> <dt>0x80070020</dt> </dl> | L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) è in uso.<br/>                                  |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ disco \_ completo)**</dt> <dt>0x80070070</dt> </dl>         | Il volume host non dispone di spazio sufficiente per la creazione di un file temporaneo necessario per la compattazione di questa immagine del disco rigido virtuale.<br/>     |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ chiusura \_ dell'app**</dt> <dt>0xA0040209</dt> </dl>                      | L'immagine del disco rigido virtuale non può essere compattata perché è in corso la chiusura dell'applicazione.<br/>                                            |
| <dl> <dt>**Macchina virtuale \_ E \_ file \_ \_**</dt> di sola lettura <dt>0xA004067A</dt> </dl>                         | L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) è contrassegnata come di sola lettura.<br/>                     |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ tipo di \_ immagine \_ HD errato**</dt> <dt>0xA004067B</dt> </dl>                   | L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) deve essere un tipo di immagine **vmDiskTypeDynamic** .<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ \_ file HD non valido**</dt> <dt>0xA0040682</dt> </dl>                        | L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) non sembra essere un'immagine valida.<br/>          |



 

## <a name="remarks"></a>Commenti

Per comprimere un'immagine del disco rigido a espansione dinamica, lo spazio disponibile nell'immagine del disco deve prima essere azzerato.

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

 

