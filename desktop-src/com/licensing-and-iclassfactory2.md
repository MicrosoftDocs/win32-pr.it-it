---
title: Licenze e IClassFactory2
description: Licenze e IClassFactory2
ms.assetid: 2bead555-8c62-4f48-a4c6-6f0942ec75f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8248b24d6b629d42e9ca631b1574c5a6719f0f4f626b2ea22792c3196c591e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096931"
---
# <a name="licensing-and-iclassfactory2"></a>Licenze e IClassFactory2

[**L'interfaccia IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) in un oggetto classe fornisce il meccanismo di creazione di oggetti di base di COM. Usando **IClassFactory,** un server può controllare la creazione di oggetti in base a un computer. L'implementazione [**del metodo IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) può consentire o non consentire la creazione di oggetti in base all'esistenza di una licenza del computer. Una licenza del computer è un'informazione separata dall'applicazione presente in un computer per indicare che il software è stato installato da un'origine valida, ad esempio i dischi di installazione del fornitore. Se la licenza del computer non esiste, il server può non consentire la creazione di oggetti. Le licenze macchina impediscono la pirateria nei casi in cui un utente tenta di copiare il software da un computer a un altro, perché le informazioni sulla licenza non vengono copiate con il software e il computer che riceve la copia non è concesso in licenza.

Tuttavia, in un settore del software componente, i fornitori necessitano di un livello di controllo più fine sulle licenze. Oltre al controllo delle licenze del computer, un fornitore deve consentire ad alcuni client di creare un oggetto componente negando la stessa funzionalità ad altri client. A questo scopo, l'applicazione client deve ottenere una chiave di licenza dal componente mentre l'applicazione client è ancora in fase di sviluppo. L'applicazione client usa il codice di licenza in fase di esecuzione per creare oggetti in un computer senza licenza.

Ad esempio, se un fornitore fornisce una libreria di controlli agli sviluppatori, lo sviluppatore che acquista la libreria avrà una licenza completa del computer, consentendo la creazione degli oggetti nel computer di sviluppo. Lo sviluppatore può quindi compilare un'applicazione client nel computer concesso in licenza incorporando uno o più controlli. Quando l'applicazione client risultante viene eseguita in un altro computer, i controlli usati nell'applicazione client devono essere creati nell'altro computer anche se tale computer non dispone di una licenza computer per i controlli del fornitore originale.

[**L'interfaccia IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) fornisce questo livello di controllo. Per consentire le licenze basate su chiave per un determinato componente, implementare **IClassFactory2** nell'oggetto class factory per tale componente. **IClassFactory2** deriva da [**IClassFactory,**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)quindi implementando **IClassFactory2,** l'oggetto class factory soddisfa i requisiti COM di base.

Per incorporare un componente concesso in licenza nell'applicazione client, usare i metodi seguenti in [**IClassFactory2:**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)

-   Il [**metodo GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) riempie una [**struttura LICINFO**](/windows/win32/api/ocidl/ns-ocidl-licinfo) con informazioni che descrivono il comportamento delle licenze del class factory. Ad esempio, il class factory può fornire codici di licenza per le licenze in fase di esecuzione se il membro **fRunTimeKeyAvail** è **TRUE.**
-   Il [**metodo RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) fornisce una chiave di licenza per il componente. Una licenza del computer deve essere disponibile quando il client chiama questo metodo.
-   Il [**metodo CreateInstanceLic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) crea un'istanza del componente concesso in licenza se il parametro della chiave di licenza (BSTRÂ bstrKey) è valido.

> [!Note]  
> Nelle informazioni sul tipo, un componente usa l'attributo concesso in licenza per contrassegnare la coclasse che supporta le licenze tramite [**IClassFactory2.**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)

 

In primo luogo, è necessario uno strumento di sviluppo separato che sia anche un client del componente concesso in licenza. Lo scopo di questo strumento è ottenere il codice di licenza di run-time e salvarlo nell'applicazione client. Questo strumento viene eseguito solo in un computer che dispone di una licenza del computer per il componente. Lo strumento chiama i [**metodi GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) e [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) per ottenere la chiave di licenza di run-time e quindi salva la chiave di licenza nell'applicazione client. Ad esempio, lo strumento di sviluppo potrebbe creare un file di intestazione (con estensione h) contenente la chiave di licenza BSTR e quindi includere tale file con estensione h nell'applicazione client.

Per creare un'istanza del componente all'interno dell'applicazione client, provare prima di tutto a creare un'istanza dell'oggetto direttamente con [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance). Se **CreateInstance ha** esito positivo, il secondo computer viene concesso in licenza per il componente e gli oggetti possono essere creati in base alle regole. Se **CreateInstance ha** esito negativo con il codice restituito CLASS \_ E NOTLICENSED, l'unico modo per creare l'oggetto è passare la chiave di run-time al metodo \_ [**CreateInstanceLic.**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) **CreateInstanceLic** verifica la chiave e crea l'oggetto se la chiave è valida.

In questo modo, un'applicazione compilata con componenti (ad esempio i controlli) può essere eseguita in un computer che non dispone di altre licenze. Solo l'applicazione client che contiene la licenza di run-time può creare gli oggetti componente in questione.

[**L'interfaccia IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) supporta la flessibilità negli schemi di licenza. Ad esempio, l'implementatore del server può crittografare le chiavi di licenza nel componente per una sicurezza aggiunta. Gli implementatori del server possono anche abilitare o disabilitare i livelli di funzionalità nei propri oggetti fornendo codici di licenza diversi per funzioni diverse. Ad esempio, una chiave potrebbe consentire un livello di base di funzionalità, mentre un'altra consente funzionalità di base e avanzate e così via.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Responsabilità del server COM](com-server-responsibilities.md)
</dt> </dl>

 

 