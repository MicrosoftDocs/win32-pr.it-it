---
title: Interfaccia IDWriteTextFormat1
description: Descrive le proprietà dei tipi di carattere e paragrafi usati per formattare il testo e descrive le informazioni sulle impostazioni locali. | Interfaccia IDWriteTextFormat1
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- Scrittura diretta dell'interfaccia IDWriteTextFormat1
- Scrittura diretta dell'interfaccia IDWriteTextFormat1, descritta
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321247"
---
# <a name="idwritetextformat1-interface"></a>Interfaccia IDWriteTextFormat1

Descrive le proprietà dei tipi di carattere e paragrafi usati per formattare il testo e descrive le informazioni sulle impostazioni locali. Questa interfaccia ha tutti gli stessi metodi di [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e aggiunge la possibilità di applicare un orientamento esplicito.

## <a name="members"></a>Membri

L'interfaccia **IDWriteTextFormat1** eredita da [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat). **IDWriteTextFormat1** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDWriteTextFormat1** dispone di questi metodi.



| Metodo                                                                                | Descrizione                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | Ottiene il fallback corrente. Se non è stato impostato alcun valore dopo la creazione del layout, sarà nullptr.<br/>               |
| [**GetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | Ottiene la modalità di wrapping dell'ultima riga.<br/>                                                                     |
| [**GetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | Ottiene l'allineamento del margine ottico per il formato di testo.<br/>                                                       |
| [**GetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | Ottiene l'orientamento preferito dei glifi quando si usa una direzione di lettura verticale.<br/>                             |
| [**SetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | Applica il fallback del tipo di carattere personalizzato nel layout. Se non è impostato alcun oggetto, viene utilizzato l'elenco di fallback di sistema predefinito. <br/> |
| [**SetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | Imposta la modalità di wrapping dell'ultima riga.<br/>                                                                     |
| [**SetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | Imposta l'allineamento del margine ottico per il formato di testo.<br/>                                                       |
| [**SetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | Imposta l'orientamento di un formato di testo.<br/>                                                                       |



 

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

[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

