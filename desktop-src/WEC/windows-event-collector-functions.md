---
title: Funzioni dell'agente di raccolta eventi di Windows
description: Nell'elenco seguente vengono descritte brevemente le funzioni utilizzate nell'agente di raccolta eventi di Windows.
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c20e3bbee6226d385681c7471bb7fd3f337dfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328300"
---
# <a name="windows-event-collector-functions"></a>Funzioni dell'agente di raccolta eventi di Windows

Nell'elenco seguente vengono descritte brevemente le funzioni utilizzate nell'agente di raccolta eventi di Windows.

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

Recupera il numero di indici della matrice di valori di proprietà per le origini eventi di una sottoscrizione.

</dd> <dt>

[**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

Recupera un valore di proprietà da un oggetto sottoscrizione.

</dd> <dt>

[**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

Recupera le informazioni sullo stato della fase di esecuzione per un'origine evento di una sottoscrizione o la sottoscrizione stessa.

</dd> <dt>

[**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

Inserisce un oggetto vuoto in una matrice di valori di proprietà per le origini eventi di una sottoscrizione.

</dd> <dt>

[**EcOpenSubscriptionEnum**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

Crea un enumeratore di sottoscrizioni per enumerare tutte le sottoscrizioni registrate nel computer locale.

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

Imposta un valore della proprietà in una matrice di valori di proprietà per le origini eventi di una sottoscrizione.

</dd> <dt>

[**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

Imposta nuovi valori o aggiorna i valori esistenti di una sottoscrizione.

</dd> <dt>

[**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

Rimuove un elemento da una matrice di oggetti che contengono valori di proprietà per le origini eventi di una sottoscrizione.

</dd> <dt>

[**EcRetrySubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

Tentativi di connessione all'origine evento di una sottoscrizione non connessa.

</dd> </dl>

 

 




