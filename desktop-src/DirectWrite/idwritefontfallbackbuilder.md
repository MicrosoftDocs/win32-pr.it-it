---
title: Interfaccia IDWriteFontFallbackBuilder
description: Consente di creare mapping di fallback dei tipi di carattere Unicode e di creare un oggetto di fallback dei tipi di carattere da tali mapping.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Interfaccia IDWriteFontFallbackBuilder Direct Write
- Interfaccia IDWriteFontFallbackBuilder Direct Write, descritta
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
ms.openlocfilehash: 3f42bc9882c238bb1167c76e941c4f183eef05e12d5d8dc70305b0c01e048797
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051392"
---
# <a name="idwritefontfallbackbuilder-interface"></a>Interfaccia IDWriteFontFallbackBuilder

Consente di creare mapping di fallback dei tipi di carattere Unicode e di creare un oggetto di fallback dei tipi di carattere da tali mapping.

## <a name="members"></a>Membri

**L'interfaccia IDWriteFontFallbackBuilder** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDWriteFontFallbackBuilder** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDWriteFontFallbackBuilder** include questi metodi.



| Metodo                                                                      | Descrizione                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AddMapping**](idwritefontfallbackbuilder-addmapping.md)                 | Aggiunge un singolo mapping all'elenco. Chiamare questa operazione una volta per ogni mapping aggiuntivo.<br/> |
| [**AddMappings**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | Aggiungere tutti i mapping da un oggetto di fallback del tipo di carattere esistente.<br/>                       |
| [**CreateFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | Crea l'oggetto di fallback finalizzato dai mapping aggiunti.<br/>                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | Windows Server 2012 App desktop R2 \[ \| per app UWP\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

