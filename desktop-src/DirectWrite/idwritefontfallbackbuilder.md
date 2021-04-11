---
title: Interfaccia IDWriteFontFallbackBuilder
description: Consente di creare mapping di fallback dei tipi di carattere Unicode e di creare un oggetto del tipo di carattere che esegue il fallback da tali mapping.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Scrittura diretta dell'interfaccia IDWriteFontFallbackBuilder
- Scrittura diretta dell'interfaccia IDWriteFontFallbackBuilder, descritta
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38cd1770bdd9617f53bb48d725b55c466b12c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964456"
---
# <a name="idwritefontfallbackbuilder-interface"></a>Interfaccia IDWriteFontFallbackBuilder

Consente di creare mapping di fallback dei tipi di carattere Unicode e di creare un oggetto del tipo di carattere che esegue il fallback da tali mapping.

## <a name="members"></a>Membri

L'interfaccia **IDWriteFontFallbackBuilder** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDWriteFontFallbackBuilder** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDWriteFontFallbackBuilder** dispone di questi metodi.



| Metodo                                                                      | Descrizione                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AddMapping**](idwritefontfallbackbuilder-addmapping.md)                 | Accoda un singolo mapping all'elenco. Chiamare questa volta per ogni mapping aggiuntivo.<br/> |
| [**AddMappings**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | Aggiungere tutti i mapping da un oggetto fallback del tipo di carattere esistente.<br/>                       |
| [**CreateFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | Crea l'oggetto fallback finalizzato dai mapping aggiunti.<br/>                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

