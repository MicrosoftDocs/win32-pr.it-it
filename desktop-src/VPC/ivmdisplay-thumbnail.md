---
title: Proprietà IVMDisplay Thumbnail (VPCCOMInterfaces.h)
description: Recupera una matrice di pixel che rappresenta un'immagine di anteprima dello schermo della macchina virtuale. | Proprietà IVMDisplay Thumbnail (VPCCOMInterfaces.h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Proprietà Thumbnail Virtual PC
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
ms.openlocfilehash: a7a558a551972bb76558dcd60223d8ddc29783aeaa23e6dbe9263f34642c1c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473331"
---
# <a name="ivmdisplaythumbnail-property"></a>Proprietà IVMDisplay::Thumbnail

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una matrice di pixel che rappresenta un'immagine di anteprima dello schermo della macchina virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a>Valore proprietà

Variante di tipo VT ARRAY VT VARIANT contenente voci di tipo \_ \| \_ VT \_ UI4, una per ogni pixel nell'anteprima.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="remarks"></a>Commenti

Questa interfaccia restituisce l'anteprima in modo meno efficiente rispetto [**\_ al metodo GenerateThumbnail,**](ivmdisplay--generatethumbnail.md) ma è utilizzabile dai client di scripting. L'anteprima è sempre di 64 pixel di larghezza per 48 pixel di altezza. Ogni pixel è a 32 bit. I primi 64 elementi nella matrice sono la prima riga di pixel nell'anteprima, i 64 elementi successivi sono la seconda riga e così via.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDisplay è definito come \_ 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

