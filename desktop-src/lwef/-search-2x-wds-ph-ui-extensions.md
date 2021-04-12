---
title: Aggiunta di icone e menu di scelta rapida con le estensioni della shell
description: È possibile migliorare l'esperienza degli utenti con Microsoft Windows Desktop Search (WDS) e il gestore di protocollo implementando le estensioni della shell.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adbd6b0f4c647c47e11d14aea5e5af748a59ba53
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "104223418"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a>Aggiunta di icone e menu di scelta rapida con le estensioni della shell

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

È possibile migliorare l'esperienza degli utenti con Microsoft Windows Desktop Search (WDS) e il gestore di protocollo implementando le estensioni della shell. Senza ulteriore estensione, il gestore di protocollo creato non includerà le esperienze utente seguenti:

-   In WDS non vengono visualizzate icone specifiche per i risultati.
-   Quando si fa doppio clic su un elemento, l'interfaccia utente non risponderà all'evento.
-   Quando gli utenti fanno clic con il pulsante destro del mouse su un elemento, il menu di scelta rapida non supporta alcuna operazione per l'elemento.

Le implementazioni minime di **IPersist** e **IPersistFolder** sono richieste da **IShellFolder** ed è necessaria un'implementazione minima di **IShellFolder** per **IContextMenu** e **IExtractIcon**, le due interfacce che forniscono un'esperienza utente più trasparente.

 

## <a name="ipersist"></a>IPersist

L'interfaccia **IPersist** definisce il singolo metodo **GetClassID**, progettato per fornire il CLSID di un oggetto che può essere archiviato in modo permanente nel sistema.



| Metodo       | Descrizione                                 |
|--------------|---------------------------------------------|
| GetClassID () | Restituisce il ClassID del gestore di protocollo |



 

> [!Note]
>
> È necessario implementare lo stesso CLSID per **IPersist**, **IPersistFolder** e **IShellFolder**.

 

 

## <a name="ipersistfolder"></a>IPersistFolder

L'interfaccia **IPersistFolder** viene utilizzata per inizializzare gli oggetti cartella della shell. L'implementazione di questa interfaccia, derivata da **IPersist**, è il modo in cui viene indicato alla cartella dove si trova nello spazio dei nomi della shell.



| Metodo       | Descrizione                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| Initialize () | Indica a un oggetto cartella della shell di inizializzarsi in base alle informazioni passate e restituisce \_ OK |



 

> [!Note]
>
> È necessario implementare lo stesso CLSID per **IPersist**, **IPersistFolder** e **IShellFolder**.

 

Questa interfaccia non viene usata direttamente. Viene usato dall'implementazione file system dell'interfaccia IShellFolder:: BindToObject Quando Inizializza un oggetto cartella della shell.

 

## <a name="ishellfolder"></a>IShellFolder

L'interfaccia **IShellFolder** viene utilizzata per gestire le cartelle ed è necessaria un'implementazione parziale in modo che l'icona e le interfacce di contesto implementate per un gestore di protocollo si comportino correttamente nell'interfaccia utente dei risultati della ricerca desktop di Windows. La maggior parte delle funzionalità richieste viene esposta tramite il metodo **GetUIObjectOf** . Questo metodo consente a un componente aggiuntivo di eseguire una query per le interfacce **IExtractIcon** e **IContextMenu** .

L'interfaccia **IShellFolder** USA PIDL anziché URL. Diversamente dai requisiti di un'estensione dello spazio dei nomi completa, i componenti aggiuntivi possono utilizzare una semplice struttura IDL che contiene solo l'URL.

È necessario implementare i metodi di **IShellFolder** seguenti. Si noti che cinque di questi metodi richiedono un'implementazione minima.



| Metodo             | Descrizione                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject ()     | Restituisce E \_ NOTIMPL                                                                                                                                                                                          |
| BindToStorage ()    | Restituisce E \_ NOTIMPL                                                                                                                                                                                          |
| CreateViewObject() | Restituisce E \_ NOTIMPL                                                                                                                                                                                          |
| SetNameOf()        | Restituisce E \_ NOTIMPL                                                                                                                                                                                          |
| ParseDisplayName () | Converte un URL nella struttura PIDL                                                                                                                                                                        |
| CompareIDs()       | Confronta due valori PIDL                                                                                                                                                                                    |
| GetDisplayNameOf () | Restituisce l'URL per un PIDL                                                                                                                                                                                  |
| GetUIObjectOf()    | Questo metodo è simile al metodo OLE COM QueryInterface. Se viene richiesta un'icona, il chiamante richiede l'IID \_ IExtractIcon; se viene richiesto un menu di scelta rapida, il chiamante richiede \_ il IContextMenu IID. |



 

> [!Note]
>
> È necessario implementare lo stesso CLSID per **IPersist**, **IPersistFolder** e **IShellFolder**.

 

**IShellFolder** non viene utilizzato per enumerare le cartelle. Ciò significa che il nome visualizzato di una cartella sarà l'URL fisico. Questo potrebbe cambiare in futuro.

 

## <a name="icontextmenu"></a>IContextMenu

Quando WDS Visualizza i risultati per l'utente, l'utente può fare clic con il pulsante destro del mouse su un elemento e visualizzare un menu di scelta rapida definito dall'interfaccia **IContextMenu** .

L'azione predefinita nel menu di scelta rapida è identica a quella eseguita quando si fa doppio clic sull'elemento. Senza le interfacce **IShellFolder** o **IContextMenu** corrispondenti per l'elemento, il comportamento predefinito per un evento di doppio clic consiste nel passare l'URL come argomento alla funzione ShellExecute.

 

## <a name="iextracticon"></a>IExtractIcon

**IExtractIcon** recupera un'icona per l'interfaccia utente di WDS basata sull'URL nel PIDL fornito dal gestore del protocollo.

 

## <a name="code-sample"></a>Codice di esempio

Il [codice di esempio dell'interfaccia utente del gestore di protocollo personalizzato](-search-2x-wds-ph-ui-samplecode.md) illustra un'implementazione di **IShellFolder** e le interfacce di supporto e include il supporto per la modifica di PIDL.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Codice di esempio dell'interfaccia utente del gestore di protocollo personalizzato](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installazione e registrazione di gestori di protocollo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




