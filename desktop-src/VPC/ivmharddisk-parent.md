---
title: Proprietà padre IVMHardDisk (VPCCOMInterfaces. h)
description: Elemento padre del disco rigido virtuale differenze.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Proprietà padre Virtual PC
- Proprietà padre Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, proprietà Parent
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963727"
---
# <a name="ivmharddiskparent-property"></a>IVMHardDisk::P proprietà adre

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e imposta l'elemento padre del disco rigido virtuale differenze.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a>Valore proprietà

Imposta l'oggetto [**IVMHardDisk**](ivmharddisk.md) associato all'immagine del disco rigido padre.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                                                                                                                                                              |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **null**.<br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                               | Non si tratta di un disco rigido differenze, pertanto non dispone di un elemento padre.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt> </dl> | Il sistema non è riuscito a trovare il file del disco rigido virtuale padre.<br/>                                                                                                                                                                                                               |
| <dl> <dt>HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)</dt> <dt>0 x 80070003</dt> </dl> | Il sistema non è riuscito a trovare il percorso del file del disco rigido virtuale padre.<br/>                                                                                                                                                                                                   |
| <dl> <dt>Macchina virtuale \_ E \_ \_ immagine HD \_ \_ non riuscita</dt> <dt>0xA004067C</dt> </dl>                  | Si è verificato un errore durante il tentativo di aprire il file di immagine del disco rigido corrente.<br/>                                                                                                                                                                                               |
| <dl> <dt>Macchina virtuale \_ E \_ \_ \_ accesso alle immagini HD</dt> <dt>0xA0040681</dt> </dl>                      | Si è verificato un errore durante il tentativo di accesso al file di immagine del disco rigido corrente.<br/>                                                                                                                                                                                             |
| <dl> <dt>Macchina virtuale \_ \_ID figlio padre E non \_ \_ \_ corrispondente</dt> <dt>0xA0040685</dt> </dl>            | L'immagine del disco rigido virtuale individuata dal parametro *padre* non ha lo stesso ID dell'immagine del disco figlio. Verificare che l'immagine del disco rigido virtuale padre individuata dal parametro *padre* sia la stessa immagine usata per creare l'immagine del disco rigido virtuale differenze.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Commenti

Questa proprietà è valida solo con le immagini del disco rigido differenze.

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

 

