---
title: Codici di errore specifici di WCS
description: Di seguito è riportato un elenco di codici di errore correlati in modo specifico all'uso di WCS 1.0.
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46127e27b0f0890e305fee65534b0cce743c086e9e89934797bf2b16b15e9f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814601"
---
# <a name="error-codes-specific-to-wcs"></a>Codici di errore specifici di WCS

Di seguito è riportato un elenco di codici di errore correlati in modo specifico all'uso di WCS 1.0. Questo non significa che le funzioni WCS restituiranno solo questi codici di errore. Ciò significa che i codici nella tabella seguente vengono restituiti solo dalle funzioni WCS. Possono anche restituire altri codici di errore Win32 documentati altrove nell'API Win32 di Platform SDK.

<dl> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>ERRORE \_ DURANTE \_ L'ELIMINAZIONE ICM \_ XFORM
</dt> <dd>

Impossibile eliminare la trasformazione colore specificata.

</dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>ERRORE \_ TAG \_ DUPLICATO
</dt> <dd>

Il tag dell'elemento del profilo colori specificato è già presente nel profilo colori.

</dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ERRORE \_ ICM \_ NON \_ ABILITATO
</dt> <dd>

Gestione colori immagine non è attualmente abilitata.

</dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERRORE \_ \_ CMM NON VALIDO
</dt> <dd>

Il nome file specificato non fa riferimento a un modulo di gestione colori valido.

</dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERRORE \_ DI \_ COLORSPACE NON VALIDO
</dt> <dd>

Lo spazio colori specificato non è valido.

</dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERRORE \_ PROFILO NON \_ VALIDO
</dt> <dd>

Il nome file specificato non fa riferimento a un profilo colori valido.

</dd> <dt>

<span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>ERRORE \_ TRASFORMAZIONE NON \_ VALIDA 
</dt> <dd>

La trasformazione del colore specificata non è una trasformazione di colore valida.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>PROFILO \_ DI ERRORE NON ASSOCIATO AL \_ \_ \_ \_ DISPOSITIVO
</dt> <dd>

Il profilo colori specificato non è associato ad alcun dispositivo.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>PROFILO \_ DI ERRORE NON \_ \_ TROVATO 
</dt> <dd>

Il nome file del profilo colori specificato non è stato trovato. Il nome o il percorso del file non è corretto.

</dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>TAG \_ DI ERRORE NON \_ \_ TROVATO
</dt> <dd>

Il tag dell'elemento del profilo colori specificato non è stato trovato nel profilo colori.

</dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>TAG \_ DI ERRORE NON \_ \_ PRESENTE
</dt> <dd>

Un tag dell'elemento del profilo colori necessario per la riuscita della funzione non è stato passato alla funzione.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Costanti WCS](wcs-constants.md)
</dt> </dl>

 

 




