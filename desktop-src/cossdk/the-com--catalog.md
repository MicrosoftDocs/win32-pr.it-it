---
description: Il catalogo COM+ archivia gli attributi dell'applicazione COM+, gli attributi della classe e gli attributi a livello di computer. Garantisce la coerenza tra questi attributi e fornisce operazioni comuni su questi attributi.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: Catalogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304607"
---
# <a name="the-com-catalog"></a>Catalogo COM+

Il catalogo COM+ archivia gli attributi dell'applicazione COM+, gli attributi della classe e gli attributi a livello di computer. Garantisce la coerenza tra questi attributi e fornisce operazioni comuni su questi attributi.

Il catalogo COM+ utilizza due archivi diversi, come indicato di seguito:

-   Database di registrazione COM+
-   Registro di sistema di Windows (**\_ \_ radice delle classi HKEY**)

Il catalogo presenta una visualizzazione logica unificata di questi due archivi e li espone tramite la libreria di amministrazione COM+. Questa libreria fornisce, tramite un linguaggio di scripting, tutte le funzionalità dello strumento di amministrazione Servizi componenti.

Per i componenti COM esistenti che non richiedono alcun nuovo servizio COM+, la ricerca viene eseguita nel registro di sistema di Windows esistente. Il catalogo COM+ usa anche il registro di sistema di Windows per la registrazione di librerie dei tipi e proxy/stub di interfaccia.

## <a name="split-registration"></a>Suddivisione registrazione

Per i nuovi componenti che sono effettivamente già componenti COM esistenti utilizzati nell'ambiente dei servizi (ad esempio, i componenti MTS), l'aspetto COM di base della registrazione viene archiviato nel registro di sistema di Windows e i nuovi servizi e attributi (ad esempio, i componenti in coda) vengono archiviati nel database di registrazione COM+. Questa operazione è nota come *registrazione Split*.

Ogni attributo viene archiviato in una sola posizione, ovvero il registro di sistema di Windows o il database di registrazione COM+. I nuovi componenti COM vengono registrati esclusivamente nel database di registrazione COM+, con alcune duplicazioni nel registro di sistema di Windows, in modo che gli strumenti esistenti possano usarli.

## <a name="transactional-updates-to-the-catalog"></a>Aggiornamenti transazionali al catalogo

Alcune operazioni nel catalogo vengono eseguite in modo transazionale. Quando si richiama la libreria di amministrazione COM+ da un componente transazionale, gli aggiornamenti al database di registrazione COM+ avvengono all'interno del limite della transazione del componente chiamante.

Tuttavia, gli aggiornamenti che comportano modifiche ad altri archivi, ad esempio il file system e il registro di sistema di Windows, non sono necessariamente completamente transazionali. Una transazione interrotta può lasciare questi archivi in uno stato non coerente con le modifiche apportate l'una all'altra o al database di registrazione COM+.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di pacchetti di installazione per applicazioni COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Distribuzione di proxy di applicazione](deploying-application-proxies.md)
</dt> <dt>

[Utilità di replica COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



