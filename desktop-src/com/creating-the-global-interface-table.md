---
title: Creazione della tabella di interfaccia globale
description: Creazione della tabella di interfaccia globale
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836cc5507ac9b8e7cccd6e9dc8fd8c2d71e1a23419945ecc01d35b3978940124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793771"
---
# <a name="creating-the-global-interface-table"></a>Creazione della tabella di interfaccia globale

Usare la chiamata seguente per creare l'oggetto tabella di interfaccia globale e ottenere un puntatore a [**IGlobalInterfaceTable:**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable)

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
> Quando si crea l'oggetto tabella di interfaccia globale usando la chiamata precedente, è necessario collegarsi alla libreria uuid.lib. Verranno risolti i simboli esterni CLSID \_ StdGlobalInterfaceTable e IID \_ IGlobalInterfaceTable.

 

Esiste una singola istanza della tabella di interfaccia globale per processo, quindi tutte le chiamate a questa funzione in un processo restituiscono la stessa istanza.

Dopo la chiamata alla [**funzione CoCreateInstance,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) registrare l'interfaccia dall'apartment in cui si trova con una chiamata al [**metodo RegisterInterfaceInGlobal.**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) Questo metodo fornisce un cookie che identifica l'interfaccia e la relativa posizione. Un apartment che cerca un puntatore a questa interfaccia chiama quindi il metodo [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) con questo cookie e l'implementazione fornisce quindi un puntatore a interfaccia all'apartment chiamante. Per revocare la registrazione globale dell'interfaccia, qualsiasi apartment può chiamare il [**metodo RevokeInterfaceFromGlobal.**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal)

Un semplice esempio dell'uso di [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) è quando si vuole passare un puntatore a interfaccia su un oggetto in un apartment a thread singolo (STA) a un thread di lavoro in un altro apartment. Anziché effettuare il marshalling in un flusso e passare il flusso al thread di lavoro come parametro del thread, **IGlobalInterfaceTable** consente semplicemente di passare un cookie.

Quando si registra l'interfaccia nella tabella di interfaccia globale, si ottiene un cookie che è possibile usare invece di passare il puntatore effettivo (ogni volta che è necessario passare il puntatore), a un parametro non metodo che passa a un altro apartment (come parametro a [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) tramite [**CreateThread)**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)o alla memoria in-process accessibile all'esterno dell'apartment.

È necessario fare attenzione perché l'uso di interfacce globali pone il carico aggiuntivo sul programmatore di gestire problemi come race conditions ed esclusione reciproca, associati all'accesso allo stato globale da più thread contemporaneamente.

COM fornisce un'implementazione standard [**dell'interfaccia IGlobalInterfaceTable.**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) È consigliabile usare questa implementazione standard perché fornisce funzionalità thread-safe complete.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Quando usare la tabella di interfaccia globale](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 