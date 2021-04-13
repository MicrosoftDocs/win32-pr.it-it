---
title: Licenze e IClassFactory2
description: Licenze e IClassFactory2
ms.assetid: 2bead555-8c62-4f48-a4c6-6f0942ec75f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9376d5187588ba14da434161309409bf1d189a8f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399778"
---
# <a name="licensing-and-iclassfactory2"></a>Licenze e IClassFactory2

L'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) su un oggetto classe fornisce il meccanismo di creazione di oggetti di base di com. Utilizzando **IClassFactory**, un server può controllare la creazione di oggetti in base a un computer. L'implementazione del metodo [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) può consentire o impedire la creazione di oggetti in base all'esistenza di una licenza computer. Una licenza per computer è una parte di informazioni separate dall'applicazione presente in un computer per indicare che il software è stato installato da un'origine valida, ad esempio i dischi di installazione del fornitore. Se la licenza del computer non esiste, il server può impedire la creazione di oggetti. Il servizio licenze Machine impedisce la pirateria nei casi in cui un utente tenta di copiare il software da un computer a un altro, perché le informazioni sulle licenze non vengono copiate con il software e il computer che riceve la copia non è concesso in licenza.

Tuttavia, in un settore software componente, i fornitori necessitano di un livello di controllo più preciso sulle licenze. Oltre al controllo delle licenze del computer, un fornitore deve consentire ad alcuni client di creare un oggetto componente negando agli altri client la stessa funzionalità. Questa operazione richiede che l'applicazione client ottenga un codice di licenza dal componente mentre l'applicazione client è ancora in fase di sviluppo. L'applicazione client usa il codice di licenza in fase di esecuzione per creare oggetti in una macchina senza licenza.

Se, ad esempio, un fornitore fornisce una libreria di controlli per gli sviluppatori, lo sviluppatore che acquista la libreria disporrà di una licenza di computer completa, consentendo la creazione degli oggetti nel computer di sviluppo. Lo sviluppatore può quindi compilare un'applicazione client nel computer con licenza che include uno o più controlli. Quando l'applicazione client risultante viene eseguita in un altro computer, i controlli utilizzati nell'applicazione client devono essere creati nell'altro computer anche se tale computer non dispone di una licenza computer per i controlli del fornitore originale.

L'interfaccia [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) fornisce questo livello di controllo. Per consentire la gestione delle licenze basate su chiavi per un determinato componente, implementare **IClassFactory2** nell'oggetto class factory per quel componente. **IClassFactory2** deriva da [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), quindi implementando **IClassFactory2**, l'oggetto class factory soddisfa i requisiti com di base.

Per incorporare un componente concesso in licenza nell'applicazione client, usare i metodi seguenti in [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2):

-   Il metodo [**GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) riempie una struttura [**LICINFO**](/windows/win32/api/ocidl/ns-ocidl-licinfo) con informazioni che descrivono il comportamento di gestione delle licenze del class factory. Ad esempio, il class factory può fornire i codici di licenza per le licenze di run-time se il membro **fRunTimeKeyAvail** è **true**.
-   Il metodo [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) fornisce un codice di licenza per il componente. Quando il client chiama questo metodo, deve essere disponibile una licenza computer.
-   Il metodo [**CreateInstanceLic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) crea un'istanza del componente concesso in licenza se il parametro della chiave di licenza (BSTRÂ bstrKey) è valido.

> [!Note]  
> Nelle informazioni sul tipo, un componente usa l'attributo concesso in licenza per contrassegnare la coclasse che supporta la gestione delle licenze tramite [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2).

 

Per prima cosa, è necessario uno strumento di sviluppo separato che sia anche un client del componente concesso in licenza. Lo scopo di questo strumento è ottenere il codice di licenza della fase di esecuzione e salvarlo nell'applicazione client. Questo strumento viene eseguito solo in un computer che dispone di una licenza computer per il componente. Lo strumento chiama i metodi [**GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) e [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) per ottenere il codice di licenza della fase di esecuzione e quindi Salva la chiave di licenza nell'applicazione client. Lo strumento di sviluppo, ad esempio, può creare un file di intestazione (con estensione h) contenente il codice di licenza BSTR e quindi includere il file con estensione h nell'applicazione client.

Per creare un'istanza del componente all'interno dell'applicazione client, provare innanzitutto a creare un'istanza dell'oggetto direttamente con [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance). Se **CreateInstance** riesce, il secondo computer viene concesso in licenza per il componente e gli oggetti possono essere creati in. Se **CreateInstance** ha esito negativo con la classe di codice restituito \_ E \_ NOTLICENSED, l'unico modo per creare l'oggetto è passare la chiave della fase di esecuzione al metodo [**CreateInstanceLic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) . **CreateInstanceLic** verifica la chiave e crea l'oggetto se la chiave è valida.

In questo modo, un'applicazione compilata con componenti, ad esempio i controlli, può essere eseguita in un computer che non dispone di altre licenze. solo l'applicazione client che contiene la licenza di runtime è autorizzata a creare gli oggetti componente in questione.

L'interfaccia [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) supporta la flessibilità negli schemi di gestione delle licenze. L'implementatore del server può ad esempio crittografare le chiavi di licenza nel componente per una maggiore sicurezza. Gli implementatori di server possono anche abilitare o disabilitare i livelli di funzionalità nei rispettivi oggetti fornendo codici di licenza diversi per le diverse funzioni. Ad esempio, una chiave potrebbe consentire un livello di base di funzionalità, mentre un'altra consente funzionalità di base e avanzate e così via.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Responsabilità server COM](com-server-responsibilities.md)
</dt> </dl>

 

 