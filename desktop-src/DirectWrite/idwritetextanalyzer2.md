---
title: Interfaccia IDWriteTextAnalyzer2
description: Analizza varie proprietà di testo per l'elaborazione di script complessi.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- Interfaccia IDWriteTextAnalyzer2 Direct Write
- Interfaccia Direct Write di IDWriteTextAnalyzer2 , descritta
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a76d4b4b7c2ef09f82834ed2e7f40ee89d2ab80bd0595db62790f38831b86fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075571"
---
# <a name="idwritetextanalyzer2-interface"></a>Interfaccia IDWriteTextAnalyzer2

Analizza varie proprietà di testo per l'elaborazione di script complessi.

## <a name="members"></a>Membri

**L'interfaccia IDWriteTextAnalyzer2** eredita da [**IDWriteTextAnalyzer1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) **IDWriteTextAnalyzer2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDWriteTextAnalyzer2** include questi metodi.



| Metodo                                                                                    | Descrizione                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**CheckTypographicFeature**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | Controlla se è disponibile una funzionalità tipografica per un glifo o un set di glifi.<br/> |
| [**GetGlyphOrientationTransform**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | Restituisce una matrice di trasformazione 2x3 per il rispettivo angolo per disegnare l'esecuzione del glifo.<br/> |
| [**GetTypographicFeatures**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | Restituisce un elenco completo delle funzionalità OpenType disponibili per uno script o un tipo di carattere.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

