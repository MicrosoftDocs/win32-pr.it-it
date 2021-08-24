---
title: Proprietà padre IVMHardDisk (VPCCOMInterfaces.h)
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
ms.openlocfilehash: 3e0ba8d56ad09f7c8263e41b17d2e107a0a441408d22ffb604e95055c57fb21d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472101"
---
# <a name="ivmharddiskparent-property"></a>Proprietà IVMHardDisk::P arent

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

Imposta [**l'oggetto IVMHardDisk**](ivmharddisk.md) associato all'immagine del disco rigido padre.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                                                                                                                                                              |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **NULL.**<br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                               | Non si tratta di un disco rigido differenze, quindi non ha un elemento padre.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0x80070002</dt> </dl> | Il sistema non è stato in grado di trovare il file del disco rigido virtuale padre.<br/>                                                                                                                                                                                                               |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)</dt> <dt>0x80070003</dt> </dl> | Il sistema non è stato in grado di trovare il percorso del file del disco rigido virtuale padre.<br/>                                                                                                                                                                                                   |
| <dl> <dt>Macchina virtuale \_ E \_ HD IMAGE OPEN FAIL \_ \_ \_ 0xA004067C</dt> <dt></dt> </dl>                  | Si è verificato un errore durante il tentativo di aprire il file di immagine del disco rigido corrente.<br/>                                                                                                                                                                                               |
| <dl> <dt>Macchina virtuale \_ E \_ HD IMAGE ACCESS \_ \_ 0xA0040681</dt> <dt></dt> </dl>                      | Si è verificato un errore durante il tentativo di accesso al file di immagine del disco rigido corrente.<br/>                                                                                                                                                                                             |
| <dl> <dt>Macchina virtuale \_ E \_ ID FIGLIO PADRE NON \_ \_ \_ CORRISPONDENTE</dt> <dt>0xA0040685</dt> </dl>            | L'immagine del disco rigido virtuale individuata dal *parametro* padre non ha lo stesso ID dell'immagine del disco figlio. Assicurarsi che l'immagine del disco rigido virtuale padre individuata dal parametro *padre* sia la stessa usata per creare l'immagine del disco rigido virtuale differenze.<br/> |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Commenti

Questa proprietà è valida solo con immagini disco rigido differenze.

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

 

