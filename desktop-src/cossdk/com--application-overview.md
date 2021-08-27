---
description: Un'applicazione COM+ è l'unità principale di amministrazione e sicurezza per Servizi componenti ed è costituita da un gruppo di componenti COM che in genere eseguono funzioni correlate.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Cenni preliminari sull'applicazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c964d760b5ba0ef260bc9dcb0658b564a4b211075692ce6301a0445eee0eb7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991877"
---
# <a name="com-application-overview"></a>Cenni preliminari sull'applicazione COM+

Un'applicazione COM+ è l'unità principale di amministrazione e sicurezza per Servizi componenti ed è costituita da un gruppo di componenti COM che in genere eseguono funzioni correlate. Questi componenti sono costituiti ulteriormente da interfacce e metodi, come illustrato nella figura seguente.

![Diagramma che mostra le interfacce e i metodi all'interno delle caselle, in ordine di Metodo all'interno dell'interfaccia all'interno del componente all'interno dell'applicazione COM+.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

È possibile usare lo strumento amministrativo Servizi componenti per creare nuove applicazioni COM+, aggiungere componenti alle applicazioni e impostare gli attributi per un'applicazione e i relativi componenti.

Creando gruppi logici di componenti COM come applicazioni COM+, è possibile sfruttare i vantaggi seguenti di COM+:

-   Ambito di distribuzione per i componenti COM.
-   Ambito di configurazione comune per i componenti COM, inclusi i limiti di sicurezza e l'accodamento.
-   Archiviazione di attributi del componente non forniti dallo sviluppatore del componente, ad esempio transazioni e sincronizzazione.
-   Librerie a collegamento dinamico dei componenti (DLL) caricate nei processi (DLLHost.exe) su richiesta.
-   Processi del server gestito per ospitare i componenti.
-   Creazione e gestione di thread usati dai componenti.
-   Accesso all'oggetto contesto per i distributori di risorse, consentendo l'associazione automatica delle risorse acquisite al contesto. Per altre informazioni su componenti e contesti COM, vedere [Contesti COM+.](com--contexts.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni COM+](developing-com--applications.md)
</dt> <dt>

[Parti di un'applicazione COM+](parts-of-a-com--application.md)
</dt> <dt>

[Tipi di applicazioni COM+](types-of-com--applications.md)
</dt> </dl>

 

 



