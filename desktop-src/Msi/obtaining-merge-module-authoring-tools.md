---
description: Per generare un modulo unione, è necessario ottenere uno strumento software con cui modificare un file con estensione msm.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Recupero degli strumenti di creazione di moduli unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a85fb75c0317a6737393e67f12a7a03cd8b76c68a8261c9d26d10d06cbe484c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327881"
---
# <a name="obtaining-merge-module-authoring-tools"></a>Recupero degli strumenti di creazione di moduli unione

Per generare un modulo unione, è necessario ottenere uno strumento software con cui modificare un file con estensione msm. Poiché un file con estensione msm è fondamentalmente un file di .msi semplificato, è possibile usare gli stessi strumenti usati per creare un database di installazione. Ad esempio, l'applicazione Orca.exe con l'SDK Windows Installer.

Un'alternativa consiste nell'acquistare uno degli strumenti di creazione pacchetti del programma di installazione per essere disponibili da fornitori di software indipendenti. Esistono diversi strumenti di terze parti in fase di sviluppo che possono essere usati per la produzione di moduli unione. Se si sceglie di usare uno strumento di terze parti, è necessario verificare che generi moduli unione coerenti con lo standard descritto in questo documento. In particolare, è necessario determinare che gli strumenti di modifica non hanno eseguito nessuna delle operazioni seguenti nel modulo unione.

-   Aggiunta di tabelle estranee al modulo unione a cui non viene fatto riferimento nella [tabella ModuleIgnoreTable](moduleignoretable-table.md).

    Eliminare queste tabelle o aggiungerle alla tabella ModuleIgnoreTable.

-   Aggiunta di una [tabella TextStyle non necessaria](textstyle-table.md) al modulo unione.

    Se il modulo unione non ha interfaccia utente (e in genere non dovrebbe) è possibile eliminare in modo sicuro questa tabella.

-   Sono state aggiunte voci non necessarie alla [tabella Directory](directory-table.md).

    Rimuovere le voci non necessarie dalla tabella Directory.

-   Consente di non visualizzare le informazioni dalla tabella di convalida \_ del modulo unione.

    In questo modo viene impedita la convalida del modulo unione. Aggiungere una tabella \_ di convalida completa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di interfacce utente nei moduli unione](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Creazione di tabelle di directory del modulo unione](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Convalida dei moduli unione](validating-merge-modules.md)
</dt> </dl>

 

 



