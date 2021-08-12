---
description: Il catalogo COM+ archivia gli attributi dell'applicazione COM+, gli attributi della classe e gli attributi a livello di computer. Garantisce la coerenza tra questi attributi e fornisce operazioni comuni su questi attributi.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: Catalogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b345c45fddab245c1e2290dc279742ac7b3b6b25c093d677c74b232077b43ae1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305268"
---
# <a name="the-com-catalog"></a>Catalogo COM+

Il catalogo COM+ archivia gli attributi dell'applicazione COM+, gli attributi della classe e gli attributi a livello di computer. Garantisce la coerenza tra questi attributi e fornisce operazioni comuni su questi attributi.

Il catalogo COM+ usa due archivi diversi, come indicato di seguito:

-   Database di registrazione COM+
-   Registro Windows di sistema (**HKEY \_ CLASSES \_ ROOT**)

Il catalogo presenta una visualizzazione logica unificata di questi due archivi ed espone tali archivi tramite la libreria di amministrazione COM+. Questa libreria fornisce, tramite un linguaggio di scripting, tutte le funzionalità dello strumento amministrativo Servizi componenti.

Per i componenti COM esistenti che non richiedono nuovi servizi COM+, la ricerca viene eseguita nel registro Windows esistente. Il catalogo COM+ usa anche il registro Windows per la libreria dei tipi e la registrazione del proxy/stub dell'interfaccia.

## <a name="split-registration"></a>Dividere la registrazione

Per i nuovi componenti che sono effettivamente componenti COM già esistenti usati nell'ambiente dei servizi (ad esempio, componenti MTS), l'aspetto COM di base della registrazione viene archiviato nel Registro di sistema di Windows e i nuovi servizi e attributi (ad esempio, componenti in coda) vengono archiviati nel database di registrazione COM+. Questa operazione è nota come registrazione *suddivisa.*

Ogni attributo viene archiviato in un'unica posizione: il registro Windows o il database di registrazione COM+. I nuovi componenti COM vengono registrati esclusivamente nel database di registrazione COM+, con una certa duplicazione nel registro Windows in modo che gli strumenti esistenti possano usarli.

## <a name="transactional-updates-to-the-catalog"></a>Aggiornamenti transazionali al catalogo

Alcune operazioni sul catalogo vengono eseguite in modo transazionale. Quando si richiama la libreria di amministrazione COM+ da un componente transazionale, gli aggiornamenti al database di registrazione COM+ verranno esersi entro il limite della transazione del componente chiamante.

Tuttavia, non è garantito che gli aggiornamenti che comportano modifiche ad altri archivi (ad esempio il registro file system e Windows) siano completamente transazionali. Una transazione interrotta può lasciare questi archivi in uno stato incoerente con le modifiche apportate l'una all'altra o al database di registrazione COM+.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di pacchetti di installazione per applicazioni COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Distribuzione di proxy di applicazione](deploying-application-proxies.md)
</dt> <dt>

[Utilità di replica COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



