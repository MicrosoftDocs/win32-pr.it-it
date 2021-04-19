---
title: Codici di errore specifici del WCS
description: Di seguito è riportato un elenco di codici di errore correlati in modo specifico all'uso di WCS 1,0.
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3040f462ce226ebd3018070abc818884cee6ad6
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/02/2021
ms.locfileid: "106320179"
---
# <a name="error-codes-specific-to-wcs"></a>Codici di errore specifici del WCS

Di seguito è riportato un elenco di codici di errore correlati in modo specifico all'uso di WCS 1,0. Questo non significa che le funzioni WCS restituiranno solo questi codici di errore. Ciò significa che i codici nella tabella seguente vengono restituiti solo dalle funzioni WCS. Possono inoltre restituire altri codici di errore Win32 documentati altrove nell'API Win32 di Platform SDK.

<dl> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>errore durante l' \_ eliminazione di \_ MCI. \_
</dt> <dd>

Non è stato possibile eliminare la trasformazione colore specificata.

</dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>ERRORE \_ tag duplicato \_
</dt> <dd>

Il tag dell'elemento del profilo colori specificato è già presente nel profilo colori.

</dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ERRORE \_ ICM \_ non \_ abilitato
</dt> <dd>

La gestione dei colori dell'immagine non è attualmente abilitata.

</dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERRORE \_ CMM non valido \_
</dt> <dd>

Il nome file specificato non fa riferimento a un modulo di gestione colori valido.

</dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERRORE \_ dello \_ spazio di colore non valido
</dt> <dd>

Lo spazio dei colori specificato non è valido.

</dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERRORE \_ profilo non valido \_
</dt> <dd>

Il nome file specificato non fa riferimento a un profilo colori valido.

</dd> <dt>

<span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>\_trasformazione errore non valida \_ 
</dt> <dd>

La trasformazione colore specificata non è una trasformazione colore valida.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>\_profilo errore \_ non \_ associato \_ al \_ dispositivo
</dt> <dd>

Il profilo colori specificato non è associato ad alcun dispositivo.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>\_profilo errore \_ non \_ trovato 
</dt> <dd>

Il nome del file del profilo colori specificato non è stato trovato. Il nome o il percorso del file non è corretto.

</dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>Tag di errore \_ \_ non \_ trovato
</dt> <dd>

Il tag dell'elemento del profilo colori specificato non è stato trovato nel profilo colori.

</dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>Tag di errore \_ \_ non \_ presente
</dt> <dd>

Un tag di elemento del profilo colori necessario per la riuscita della funzione non è stato passato alla funzione.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Costanti WCS](wcs-constants.md)
</dt> </dl>

 

 




