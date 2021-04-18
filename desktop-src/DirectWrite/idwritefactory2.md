---
title: Interfaccia IDWriteFactory2
description: Interfaccia Factory radice per tutti gli oggetti DirectWrite.
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- Scrittura diretta dell'interfaccia IDWriteFactory1
- Scrittura diretta dell'interfaccia IDWriteFactory1, descritta
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7d5ba0f8d480981ab6ebea6dcdbd955b7b967e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301932"
---
# <a name="idwritefactory2-interface"></a>Interfaccia IDWriteFactory2

Interfaccia Factory radice per tutti gli oggetti [DirectWrite](direct-write-portal.md) .

## <a name="members"></a>Membri

L'interfaccia **IDWriteFactory1** eredita da [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1). **IDWriteFactory2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDWriteFactory1** dispone di questi metodi.



| Metodo                                                                             | Descrizione                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**CreateCustomRenderingParams**](idwritefactory2-createcustomrenderingparams.md) | Crea un oggetto parametri di rendering con le proprietà specificate.<br/>                            |
| [**CreateFontFallbackBuilder**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | Crea un oggetto generatore di fallback del tipo di carattere.<br/>                                                         |
| [**CreateGlyphRunAnalysis**](idwritefactory2-createglyphrunanalysis.md)           | Crea un oggetto di analisi dell'esecuzione del glifo che incapsula le informazioni utilizzate per il rendering di un'esecuzione del glifo.<br/> |
| [**GetSystemFontFallback**](idwritefactory2-getsystemfontfallback.md)             | Crea un oggetto fallback del tipo di carattere dall'elenco di fallback dei tipi di carattere di sistema.<br/>                              |
| [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | Questo metodo viene chiamato su un'esecuzione di glifo per tradurlo in più esecuzioni di glifi a più colori.<br/>           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

