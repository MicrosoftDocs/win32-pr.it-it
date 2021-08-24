---
title: Metodo _GenerateThumbnail IVMDisplay (VPCCOMInterfaces.h)
description: Recupera una matrice di pixel che rappresenta un'immagine di anteprima dello schermo della macchina virtuale. | Metodo _GenerateThumbnail IVMDisplay (VPCCOMInterfaces.h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- _GenerateThumbnail virtual PC
- _GenerateThumbnail metodo Virtual PC , interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC , _GenerateThumbnail metodo
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
ms.openlocfilehash: 5decd1b3c55ab6513408a81eb37d422fac495334fb545c4cad4806050a8af7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654371"
---
# <a name="ivmdisplay_generatethumbnail-method"></a>Metodo IVMDisplay:: \_ GenerateThumbnail

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una matrice di pixel che rappresenta un'immagine di anteprima dello schermo della macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*thumbnailImage* \[ Cambio\]
</dt> <dd>

Matrice di pixel che rappresenta un'immagine di anteprima dello schermo della macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>        |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia restituisce l'anteprima in modo più efficiente rispetto [**alla proprietà Thumbnail,**](ivmdisplay-thumbnail.md) ma non può essere utilizzata dai client di scripting. L'anteprima ha sempre una larghezza di 64 pixel per 48 pixel di altezza. Ogni pixel è a 32 bit, dove gli 8 bit superiori rappresentano il valore blu del pixel, gli 8 bit successivi rappresentano il valore verde del pixel e gli 8 bit successivi rappresentano il valore rosso del pixel. I primi 64 elementi nella matrice sono la prima riga dell'anteprima, i 64 elementi successivi sono la seconda riga e così via. Questo metodo restituisce una matrice statica di pixel, che è più efficiente rispetto alla restituzione di **un SAFEARRAY** di valori **VARIANT,** ma non è compatibile con i client di scripting.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

