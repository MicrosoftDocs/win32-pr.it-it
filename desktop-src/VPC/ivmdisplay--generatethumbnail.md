---
title: Metodo _GenerateThumbnail IVMDisplay (VPCCOMInterfaces. h)
description: Recupera una matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale. | Metodo _GenerateThumbnail IVMDisplay (VPCCOMInterfaces. h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- Metodo di _GenerateThumbnail Virtual PC
- Metodo _GenerateThumbnail Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, metodo _GenerateThumbnail
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4084549de96330761bca4f4ec6da65ca150c96e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321661"
---
# <a name="ivmdisplay_generatethumbnail-method"></a>Metodo IVMDisplay:: \_ GenerateThumbnail

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera una matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*thumbnailImage* \[ out\]
</dt> <dd>

Matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>        |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia restituisce l'anteprima in modo più efficiente rispetto alla proprietà di [**Anteprima**](ivmdisplay-thumbnail.md) , ma non può essere utilizzata dai client di scripting. L'anteprima è sempre di 64 pixel in larghezza per 48 pixel di altezza. Ogni pixel è 32 bit, dove gli 8 bit superiori rappresentano il valore blu del pixel, i successivi 8 bit rappresentano il valore verde del pixel e gli 8 bit successivi rappresentano il valore rosso del pixel. I primi 64 elementi nella matrice sono la prima riga dell'anteprima, i successivi 64 elementi sono la seconda riga e così via. Questo metodo restituisce una matrice statica di pixel, che è più efficiente rispetto alla restituzione di un **SAFEARRAY** di valori **Variant** , ma non è compatibile con i client di scripting.

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

 

