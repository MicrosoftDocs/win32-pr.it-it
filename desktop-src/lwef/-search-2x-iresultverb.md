---
title: Interfaccia IResultVerb (WdsSharedIDL. h)
description: Espone le proprietà del verbo.
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultVerb
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultVerb, descritte
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301947"
---
# <a name="iresultverb-interface"></a>Interfaccia IResultVerb

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Espone le proprietà del verbo.

## <a name="members"></a>Membri

L'interfaccia **IResultVerb** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultVerb** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IResultVerb** ha queste proprietà.



| Proprietà                                                             | Tipo di accesso           | Descrizione                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](-search-2x-iresultverb-displayname.md)<br/> | Sola lettura<br/>  | Questa proprietà restituisce un puntatore al nome visualizzato localizzato per il verbo. <br/>                           |
| [**DoIt**](-search-2x-iresultverb-doit.md)<br/>               | Sola scrittura<br/> | Esegue il verbo. <br/>                                                                                    |
| [**Abilitato**](-search-2x-iresultverb-enabled.md)<br/>         | Sola lettura<br/>  | Questa proprietà restituisce TRUE se il verbo è abilitato. <br/>                                                    |
| [**HelpText**](-search-2x-iresultverb-helptext.md)<br/>       | Sola lettura<br/>  | Questa proprietà restituisce un puntatore alla stringa della Guida localizzata per il verbo. <br/>                            |
| [**Icona**](-search-2x-iresultverb-icon.md)<br/>               | Sola lettura<br/>  | Questa proprietà restituisce un puntatore per gestire l'icona facoltativa associata al verbo. <br/>              |
| [**Nome**](-search-2x-iresultverb-name.md)<br/>               | Sola lettura<br/>  | Questa proprietà restituisce un puntatore al nome cononical per il verbo, ad esempio Print, Open e così via. <br/> |



 

## <a name="remarks"></a>Commenti

Questi metodi espongono proprietà e azioni applicabili ai verbi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

