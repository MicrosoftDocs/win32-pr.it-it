---
title: Aggiunta di icone e menu di scelta rapida con le estensioni della shell
description: È possibile migliorare l'esperienza degli utenti con Microsoft Windows Desktop Search (WDS) e il gestore di protocollo implementando le estensioni della shell.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9198fc56b8ca09e61909b1828d7d00b964bb12c0e13308583eb36a4e2211f3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976871"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a>Aggiunta di icone e menu di scelta rapida con le estensioni della shell

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows ricerca.](../search/-search-3x-wds-overview.md)

È possibile migliorare l'esperienza degli utenti con Microsoft Windows Desktop Search (WDS) e il gestore di protocollo implementando le estensioni della shell. Senza altre estensioni, il gestore di protocollo creato non includerà le esperienze utente seguenti:

-   WDS non visualizza icone specifiche per i risultati.
-   Quando gli utenti fa doppio clic su un elemento, l'interfaccia utente non risponde all'evento.
-   Quando gli utenti fa clic con il pulsante destro del mouse su un elemento, il menu di scelta rapida non supporta alcuna operazione per l'elemento.

Le implementazioni minime di **IPersist** e **IPersistFolder** sono richieste da **IShellFolder** ed è necessaria un'implementazione minima di **IShellFolder** per **IContextMenu** e **IExtractIcon,** le due interfacce che offrono un'esperienza utente più semplice.

 

## <a name="ipersist"></a>Ipersist

**L'interfaccia IPersist** definisce il singolo metodo **GetClassID**, progettato per fornire il CLSID di un oggetto che può essere archiviato in modo permanente nel sistema.



| Metodo       | Descrizione                                 |
|--------------|---------------------------------------------|
| GetClassID() | Restituisce il ClassID del gestore di protocollo |



 

> [!Note]
>
> Lo stesso CLSID deve essere implementato per **IPersist,** **IPersistFolder** e **IShellFolder.**

 

 

## <a name="ipersistfolder"></a>IPersistFolder

**L'interfaccia IPersistFolder** viene usata per inizializzare gli oggetti cartella shell. L'implementazione di questa interfaccia, derivata da **IPersist,** è il modo in cui viene specificata la cartella nella posizione in cui si trova nello spazio dei nomi shell.



| Metodo       | Descrizione                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| Initialize() | Indica a un oggetto cartella shell di inizializzarsi in base alle informazioni passate e restituisce S \_ OK |



 

> [!Note]
>
> Lo stesso CLSID deve essere implementato per **IPersist,** **IPersistFolder** e **IShellFolder.**

 

Questa interfaccia non viene utilizzata direttamente. Viene usato dall'implementazione file system dell'interfaccia IShellFolder::BindToObject quando inizializza un oggetto cartella shell.

 

## <a name="ishellfolder"></a>IShellFolder

L'interfaccia **IShellFolder** viene usata per gestire le cartelle ed è necessaria un'implementazione parziale in modo che l'icona e le interfacce di contesto implementate per un gestore di protocollo si comportino correttamente nell'interfaccia utente dei risultati di Windows Desktop Search. La maggior parte delle funzionalità necessarie viene esposta tramite **il metodo GetUIObjectOf.** Questo metodo consente a un componente aggiuntivo di eseguire una query **per le interfacce IExtractIcon** **e IContextMenu.**

**L'interfaccia IShellFolder** usa PID anziché URL. A differenza dei requisiti di un'estensione dello spazio dei nomi completa, i componenti aggiuntivi possono usare una semplice struttura IDL che contiene solo l'URL.

I metodi seguenti di **IShellFolder** devono essere implementati. Si noti che cinque di questi metodi richiedono un'implementazione minima.



| Metodo             | Descrizione                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject()     | Restituisce E \_ NOTIMPL                                                                                                                                                                                          |
| BindToStorage()    | Restituisce E \_ NOTIMPL                                                                                                                                                                                          |
| CreateViewObject() | Restituisce E \_ NOTIMPL                                                                                                                                                                                          |
| SetNameOf()        | Restituisce E \_ NOTIMPL                                                                                                                                                                                          |
| ParseDisplayName() | Converte un URL nella struttura PIDL                                                                                                                                                                        |
| CompareIDs()       | Confronta due valori PIDL                                                                                                                                                                                    |
| GetDisplayNameOf() | Restituisce l'URL per un FILE PIDL                                                                                                                                                                                  |
| GetUIObjectOf()    | Questo metodo è simile al metodo OLE COM QueryInterface. Se viene richiesta un'icona, il chiamante richiede l'IID IExtractIcon. Se viene richiesto un menu di scelta rapida, il chiamante richiede \_ \_ l'IID IContextMenu. |



 

> [!Note]
>
> Lo stesso CLSID deve essere implementato per **IPersist,** **IPersistFolder** e **IShellFolder.**

 

**IShellFolder non** viene usato per enumerare le cartelle. Ciò significa che il nome visualizzato di una cartella sarà l'URL fisico. Questo potrebbe cambiare in futuro.

 

## <a name="icontextmenu"></a>IContextMenu

Quando WDS visualizza i risultati all'utente, l'utente può fare clic con il pulsante destro del mouse su un elemento e visualizzare un menu di scelta rapida definito **dall'interfaccia IContextMenu.**

L'azione predefinita nel menu di scelta rapida è la stessa eseguita quando si fa doppio clic sull'elemento. Senza le interfacce **IShellFolder** o **IContextMenu** corrispondenti per l'elemento, il comportamento predefinito per un evento di doppio clic è passare l'URL come argomento alla funzione ShellExecute.

 

## <a name="iextracticon"></a>IExtractIcon

**IExtractIcon recupera** un'icona per l'interfaccia utente di WDS in base all'URL nel file PIDL fornito dal gestore del protocollo.

 

## <a name="code-sample"></a>Codice di esempio

Il [gestore di protocollo Interfaccia utente](-search-2x-wds-ph-ui-samplecode.md) codice di esempio illustra un'implementazione di **IShellFolder** e le interfacce di supporto e include il supporto per la modifica degli PID.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Gestore di protocollo personalizzato Interfaccia utente codice di esempio](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installazione e registrazione di gestori di protocollo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




