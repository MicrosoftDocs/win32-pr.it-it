---
title: Proprietà anteprima IVMDisplay (VPCCOMInterfaces. h)
description: Recupera una matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale. | Proprietà anteprima IVMDisplay (VPCCOMInterfaces. h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Proprietà anteprima PC virtuale
- Proprietà anteprima Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, proprietà Thumbnail
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0466af2552fbb108f31de94b3f970d6e7d5571b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969037"
---
# <a name="ivmdisplaythumbnail-property"></a>Proprietà IVMDisplay:: thumbnail

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera una matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a>Valore proprietà

Variante di tipo VT \_ Array VT \| \_ Variant contenente le voci di tipo VT \_ UI4, una per ogni pixel nell'anteprima.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>        |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="remarks"></a>Commenti

Questa interfaccia restituisce l'anteprima in modo meno efficiente rispetto al metodo [**\_ GenerateThumbnail**](ivmdisplay--generatethumbnail.md) , ma può essere utilizzata dai client di scripting. L'anteprima è sempre di 64 pixel in larghezza per 48 pixel di altezza. Ogni pixel è 32 bit. I primi 64 elementi nella matrice sono la prima riga di pixel nell'anteprima, i successivi 64 elementi sono la seconda riga e così via.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

