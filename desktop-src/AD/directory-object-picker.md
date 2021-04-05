---
title: Selezione oggetti directory
description: La finestra di dialogo Selezione oggetti directory consente a un utente di selezionare uno o più oggetti dal catalogo globale, da un dominio o da un computer o da un gruppo di lavoro.
ms.assetid: 5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a
ms.tgt_platform: multiple
keywords:
- Active Directory selezione oggetti
- ANNUNCIO selezione oggetti
- oggetti AD, selezione oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f6ba7fd053aa8ab3245bf72c693f0a887aa983
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046521"
---
# <a name="directory-object-picker"></a>Selezione oggetti directory

La finestra di dialogo Selezione oggetti directory consente a un utente di selezionare uno o più oggetti dal catalogo globale, da un dominio o da un computer o da un gruppo di lavoro. I tipi di oggetto da cui un utente può selezionare includono oggetti utente, contatto, gruppo e computer. Per ulteriori informazioni su Active Directory Domain Services, vedere [Active Directory Domain Services](active-directory-domain-services.md).

Per visualizzare una finestra di dialogo di selezione oggetti:

1.  Chiamare la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) per creare un'istanza dell'interfaccia [**IDsObjectPicker**](/windows/desktop/api/Objsel/nn-objsel-idsobjectpicker) .
2.  Chiamare il metodo [**IDsObjectPicker:: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) per inizializzare la finestra di dialogo.
3.  Chiamare il metodo [**IDsObjectPicker:: InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog) per visualizzare la finestra di dialogo.
4.  Chiamare il metodo [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) dell'istanza [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) restituita dalla finestra di dialogo di selezione oggetti per recuperare i dati dell' [**elenco di \_ selezione di DSOP \_ DS \_ \_ CFSTR**](cfstr-dsop-ds-selection-list.md) . Il formato degli Appunti dell' **elenco di selezione di CFSTR \_ DSOP \_ \_ \_ DS** fornisce un **HGLOBAL** che contiene una struttura di [**\_ \_ elenco di selezione DS**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) . La struttura dell' **\_ \_ elenco di selezione DS** contiene i dati relativi agli elementi selezionati nella finestra di dialogo Selezione oggetti.

Se per un oggetto è necessario l'ID di sicurezza (SID), questo deve essere richiesto direttamente dal selettore oggetti aggiungendo l'attributo **objectSID** all'elenco di attributi da recuperare per l'oggetto selezionato. Non è consigliabile passare il nome dell'oggetto restituito alla funzione [**LsaLookupNames**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames) o [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) perché la ricerca del nome sarà ridondante e in alcuni casi potrebbe non riuscire.

Se viene salvato un riferimento a tutti gli oggetti selezionati, il nome distinto non deve essere salvato perché l'oggetto può essere spostato, rinominato o può essere modificato a causa di differenze delle impostazioni locali. Per le entità di sicurezza, il **objectSID** deve essere richiesto per l'oggetto e salvato in modo sicuro. Se il nome dell'entità di sicurezza è necessario in un secondo momento, può essere recuperato con la funzione [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) . Per tutti gli altri oggetti, il **objectGUID** deve essere richiesto e salvato.

## <a name="initialization"></a>Inizializzazione

Quando viene inizializzata la finestra di dialogo di selezione oggetti, viene specificato un set di tipi di ambito e filtri. I tipi di ambito specificati determinano i percorsi, i domini o i computer, ad esempio, da cui un utente può selezionare gli oggetti. I filtri determinano i tipi di oggetti che un utente può selezionare da un determinato tipo di ambito. Per ulteriori informazioni, vedere la sezione Scopes and filters riportata di seguito.

Per impostazione predefinita, un utente può selezionare un singolo oggetto nella finestra di dialogo Selezione oggetti directory. Per abilitare più selezioni, impostare il flag **\_ \_ MultiSelect del flag DSOP** nel membro **flOptions** della struttura delle [**\_ \_ informazioni di inizializzazione di DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info) quando la finestra di dialogo è stata inizializzata.

## <a name="scopes-and-filters"></a>Ambiti e filtri

Nell'elenco **a discesa Cerca in** sono inclusi gli ambiti da cui un utente può selezionare gli oggetti. Un ambito è un dominio, un computer, un gruppo di lavoro o un catalogo globale che archivia i dati relativi a e fornisce l'accesso a un set di oggetti disponibili. Le voci nell'elenco ambito dipendono dai tipi di ambito e dal computer di destinazione specificati quando il metodo [**IDsObjectPicker:: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) è stato chiamato per l'ultima volta per inizializzare la finestra di dialogo Selezione oggetti.

Un tipo di ambito è una categoria generica di ambiti, ad esempio tutti i domini nell'azienda a cui appartiene il computer di destinazione, o il catalogo globale per l'azienda del computer di destinazione o il computer di destinazione. Per ogni tipo di ambito specificato, nella finestra di dialogo viene utilizzato il contesto del computer di destinazione per determinare le voci dell'elenco di ambiti.

Il metodo [**IDsObjectPicker:: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) accetta un puntatore a una struttura di [**\_ \_ informazioni init DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info) che contiene una matrice di strutture di [**\_ \_ \_ informazioni di inizializzazione dell'ambito DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) . Ogni voce nella matrice **DSOP \_ scope \_ init \_ info** specifica uno o più tipi di ambito, nonché filtri applicabili e altri attributi. I filtri determinano i tipi di oggetti, ad esempio utenti, gruppi, contatti e computer, che l'utente può selezionare da un determinato tipo di ambito. Quando l'utente seleziona un ambito dall'elenco, la finestra di dialogo Applica i filtri per il tipo di ambito per visualizzare un elenco di oggetti da cui l'utente può selezionare.

Ogni struttura di [**\_ \_ \_ informazioni di inizializzazione dell'ambito DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) contiene una struttura di [**\_ \_ flag di filtro DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) che specifica i filtri per il tipo di ambito. La struttura dei **\_ \_ flag di filtro DSOP** distingue tra gli ambiti di livello superiore e inferiore:

-   Un ambito di livello superiore è un catalogo globale o un dominio che supporta il [provider LDAP](/windows/desktop/ADSI/adsi-ldap-provider)ADSI.
-   Un ambito di livello inferiore include gruppi di lavoro e tutti i singoli computer. Nella finestra di dialogo viene utilizzato il provider ADSI WinNT per accedere a un ambito di livello inferiore.

Sono disponibili due set di flag di filtro definiti per l'utilizzo nella struttura dei [**\_ \_ flag di filtro DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) : uno per gli ambiti di livello superiore e uno per gli ambiti di livello inferiore. Il membro di **livello** superiore della struttura dei **\_ \_ flag di filtro DSOP** è una struttura di [**\_ \_ \_ flag di filtro di livello superiore DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_uplevel_filter_flags) che specifica i filtri per gli ambiti di livello superiore. Il membro **flDownlevel** della struttura **dei \_ \_ flag di filtro DSOP** è un set di flag che specificano i filtri per gli ambiti di livello inferiore.

 

 