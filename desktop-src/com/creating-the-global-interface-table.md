---
title: Creazione della tabella dell'interfaccia globale
description: Creazione della tabella dell'interfaccia globale
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f792f9664da554f6522086796f94a00ccdf0dc07
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399796"
---
# <a name="creating-the-global-interface-table"></a>Creazione della tabella dell'interfaccia globale

Utilizzare la chiamata seguente per creare l'oggetto tabella dell'interfaccia globale e ottenere un puntatore a [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> Quando si crea l'oggetto tabella dell'interfaccia globale usando la chiamata precedente, è necessario collegarsi alla libreria uuid. lib. Questa operazione risolverà i simboli esterni CLSID \_ StdGlobalInterfaceTable e IID \_ IGlobalInterfaceTable.

 

Esiste una singola istanza della tabella dell'interfaccia globale per ogni processo, quindi tutte le chiamate a questa funzione in un processo restituiscono la stessa istanza.

Dopo la chiamata alla funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , registrare l'interfaccia dall'Apartment in cui risiede con una chiamata al metodo [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) . Questo metodo fornisce un cookie che identifica l'interfaccia e la relativa posizione. Un Apartment che cerca un puntatore a questa interfaccia chiama il metodo [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) con questo cookie e l'implementazione fornisce quindi un puntatore di interfaccia all'Apartment chiamante. Per revocare la registrazione globale dell'interfaccia, qualsiasi Apartment può chiamare il metodo [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) .

Un semplice esempio di utilizzo di [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) è quando si desidera passare un puntatore a un'interfaccia su un oggetto in un Apartment a thread singolo (sta) a un thread di lavoro in un altro Apartment. Anziché dover effettuare il marshalling in un flusso e passare il flusso al thread di lavoro come parametro di thread, **IGlobalInterfaceTable** consente di passare semplicemente un cookie.

Quando si registra l'interfaccia nella tabella dell'interfaccia globale, si ottiene un cookie che è possibile usare anziché passare il puntatore effettivo (ogni volta che è necessario passare il puntatore), a un parametro non di metodo che passa a un altro Apartment (come parametro a [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) tramite [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) o alla memoria in-process accessibile all'esterno dell'Apartment.

È necessario prestare attenzione perché l'uso delle interfacce globali impone un carico aggiuntivo al programmatore di gestire i problemi, ad esempio race condition ed esclusioni reciproche, associati all'accesso allo stato globale da più thread contemporaneamente.

COM fornisce un'implementazione standard dell'interfaccia [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) . Si consiglia vivamente di utilizzare questa implementazione standard perché fornisce funzionalità thread-safe complete.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Quando usare la tabella dell'interfaccia globale](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 