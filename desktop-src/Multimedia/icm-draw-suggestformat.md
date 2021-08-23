---
title: ICM_DRAW_SUGGESTFORMAT messaggio (Vfw.h)
description: Il ICM DRAW SUGGESTFORMAT esegue una query su un driver di rendering per suggerire \_ \_ un formato decompresso che può disegnare.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- ICM_DRAW_SUGGESTFORMAT messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 843dd2d398f5be6476a148922f3244113e94ab3fe3c10bac9ee08caefb8c4828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495951"
---
# <a name="icm_draw_suggestformat-message"></a>\_ICM Messaggio DRAW \_ SUGGESTFORMAT

Il **ICM \_ DRAW \_ SUGGESTFORMAT** esegue una query su un driver di rendering per suggerire un formato decompresso che può disegnare.


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*
</dt> <dd>

Puntatore a [**una struttura ICDRAWSUGGEST.**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Dimensioni, in byte, di [**ICDRAWSUGGEST.**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK in caso di esito positivo. Se il **membro lpbiSuggest** della struttura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) è **NULL,** questo messaggio restituisce la quantità di memoria necessaria per contenere il formato suggerito.

## <a name="remarks"></a>Commenti

Il driver deve esaminare il formato specificato nel membro **lpbiIn** della struttura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) e usare il membro **lpbiSuggest** per restituire un formato che può disegnare. Il formato di output deve mantenere il maggior numero possibile di dati dal formato di input.

Facoltativamente, il driver può usare l'handle di compressione installabile passato nel membro **hicDecompressor** di [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) per effettuare selezioni più complesse. Ad esempio, se il formato di input è dati JPEG a 24 bit, un renderer può eseguire una query sul decompressore per scoprire se è in grado di decomprimere in un formato YUV (che potrebbe essere disegnato in modo più efficiente) prima di selezionare il formato da suggerire.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





