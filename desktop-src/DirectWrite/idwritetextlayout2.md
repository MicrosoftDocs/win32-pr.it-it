---
title: Interfaccia IDWriteTextLayout2
description: Rappresenta un blocco di testo dopo che è stato analizzato e formattato completamente. | Interfaccia IDWriteTextLayout2
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- Interfaccia IDWriteTextLayout2 Direct Write
- Interfaccia IDWriteTextLayout2 Direct Write , descritta
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff23fea3d1ae4da7c6dba310ed28dfb8c76d65947426f0219e3868f3859c7ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816261"
---
# <a name="idwritetextlayout2-interface"></a>Interfaccia IDWriteTextLayout2

Rappresenta un blocco di testo dopo che è stato analizzato e formattato completamente.

## <a name="members"></a>Membri

**L'interfaccia IDWriteTextLayout2** eredita da [**IDWriteTextLayout1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) **IDWriteTextLayout2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDWriteTextLayout2** include questi metodi.



| Metodo                                                                                | Descrizione                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | Ottiene l'oggetto di fallback del tipo di carattere corrente. <br/>                                           |
| [**GetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | Ottiene un valore che indica se viene eseguito il wrapping dell'ultima parola nell'ultima riga.<br/>                    |
| [**GetMetrics**](idwritetextlayout2-getmetrics.md)                                   | Recupera le metriche complessive per la stringa formattata. <br/>                             |
| [**GetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | Ottenere l'allineamento dei glifi ai bordi del margine. <br/>                               |
| [**GetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | Ottenere l'orientamento preferito dei glifi quando si usa una direzione di lettura verticale.<br/> |
| [**SetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | Applicare un fallback del tipo di carattere personalizzato al layout.<br/>                                        |
| [**SetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | Impostare se viene eseguito il wrapping dell'ultima parola nell'ultima riga. <br/>                   |
| [**SetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | Impostare l'allineamento dei glifi ai bordi del margine.<br/>                                |
| [**SetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | Impostare l'orientamento preferito dei glifi quando si usa una direzione di lettura verticale.<br/> |



 

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

[**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

