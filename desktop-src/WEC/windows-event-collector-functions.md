---
title: Windows Funzioni dell'agente di raccolta eventi
description: Nell'elenco seguente vengono brevemente descritte le funzioni utilizzate nell'Windows eventi.
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17dd89cb98e3803f171633df0f902250f1147a25bce9d43c83947c2d1e83b6ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937223"
---
# <a name="windows-event-collector-functions"></a>Windows Funzioni dell'agente di raccolta eventi

Nell'elenco seguente vengono brevemente descritte le funzioni utilizzate nell'Windows eventi.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

Chiude un handle ricevuto da altre funzioni dell'agente di raccolta eventi.

</dd> <dt>

[**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)
</dt> <dd>

Elimina una sottoscrizione esistente.

</dd> <dt>

[**EcEnumNextSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription)
</dt> <dd>

Continua l'enumerazione delle sottoscrizioni registrate nel computer locale.

</dd> <dt>

[**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty)
</dt> <dd>

Recupera i valori delle proprietà per le origini eventi di una sottoscrizione.

</dd> <dt>

[**EcGetObjectArraySize**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

Recupera il numero di indici della matrice di valori di proprietà per le origini evento di una sottoscrizione.

</dd> <dt>

[**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

Recupera il valore di una proprietà da un oggetto sottoscrizione.

</dd> <dt>

[**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

Recupera le informazioni sullo stato della fase di esecuzione per un'origine evento di una sottoscrizione o della sottoscrizione stessa.

</dd> <dt>

[**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

Inserisce un oggetto vuoto in una matrice di valori di proprietà per le origini evento di una sottoscrizione.

</dd> <dt>

[**EcOpenSubscriptionEnum**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

Crea un enumeratore di sottoscrizione per enumerare tutte le sottoscrizioni registrate nel computer locale.

</dd> <dt>

[**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)
</dt> <dd>

Apre una sottoscrizione esistente o crea una nuova sottoscrizione.

</dd> <dt>

[**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
</dt> <dd>

Salva le informazioni di configurazione della sottoscrizione.

</dd> <dt>

[**EcSetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

Imposta il valore di una proprietà in una matrice di valori di proprietà per le origini evento di una sottoscrizione.

</dd> <dt>

[**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

Imposta nuovi valori o aggiorna i valori esistenti di una sottoscrizione.

</dd> <dt>

[**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

Rimuove un elemento da una matrice di oggetti che contengono valori di proprietà per le origini evento di una sottoscrizione.

</dd> <dt>

[**EcRetrySubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

Ritenta la connessione all'origine evento di una sottoscrizione non connessa.

</dd> </dl>

 

 




