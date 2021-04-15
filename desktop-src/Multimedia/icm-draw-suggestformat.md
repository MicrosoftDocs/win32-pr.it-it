---
title: Messaggio di ICM_DRAW_SUGGESTFORMAT (VFW. h)
description: Il \_ \_ messaggio SUGGESTFORMAT per il progetto ICM esegue una query su un driver di rendering per suggerire un formato decompresso che può creare.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- ICM_DRAW_SUGGESTFORMAT messaggi multimediali di Windows
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
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475701"
---
# <a name="icm_draw_suggestformat-message"></a>\_ \_ Messaggio SUGGESTFORMAT per il progetto ICM

Il **messaggio \_ \_ SUGGESTFORMAT per il progetto ICM** esegue una query su un driver di rendering per suggerire un formato decompresso che può creare.


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*
</dt> <dd>

Puntatore a una struttura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Dimensioni, in byte, di [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo. Se il membro **lpbiSuggest** della struttura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) è **null**, questo messaggio restituisce la quantità di memoria necessaria per contenere il formato suggerito.

## <a name="remarks"></a>Commenti

Il driver deve esaminare il formato specificato nel membro **lpbiIn** della struttura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) e usare il membro **lpbiSuggest** per restituire un formato che può creare. Il formato di output deve conservare il maggior quantità possibile di dati dal formato di input.

Facoltativamente, il driver può usare l'handle del compressore installabile passato nel membro **hicDecompressor** di [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) per effettuare selezioni più complesse. Se, ad esempio, il formato di input è dati JPEG a 24 bit, un renderer potrebbe eseguire una query sul decompressore per verificare se è possibile decomprimerlo in un formato YUV, che potrebbe essere disegnato in modo più efficiente, prima di selezionare il formato da suggerire.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





