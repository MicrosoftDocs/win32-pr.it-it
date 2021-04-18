---
description: Per generare un modulo merge, è necessario ottenere uno strumento software con cui modificare un file con estensione MSM.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Recupero di strumenti di creazione di moduli merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dac673c7cfa191cecb1b576e1b17f2f4a7a1f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308682"
---
# <a name="obtaining-merge-module-authoring-tools"></a>Recupero di strumenti di creazione di moduli merge

Per generare un modulo merge, è necessario ottenere uno strumento software con cui modificare un file con estensione MSM. Poiché un file con estensione MSM è fondamentalmente un file con estensione msi semplificato, potrebbe essere possibile utilizzare gli stessi strumenti utilizzati per creare un database di installazione. Ad esempio, l'applicazione Orca.exe fornita con Windows Installer SDK.

In alternativa, è possibile acquistare uno degli strumenti per la creazione di pacchetti del programma di installazione di da fornitori di software indipendenti. Sono disponibili diversi strumenti di terze parti in fase di sviluppo che possono essere utilizzati per la creazione di moduli unione. Se si sceglie di utilizzare uno strumento di terze parti, è necessario verificare che generi moduli unione coerenti con lo standard descritto in questo documento. In particolare, è necessario determinare che gli strumenti di modifica non hanno eseguito alcuna delle operazioni seguenti nel modulo merge.

-   Aggiunta di tabelle estranee al modulo merge a cui non viene fatto riferimento nella [tabella ModuleIgnoreTable](moduleignoretable-table.md).

    Eliminare queste tabelle o aggiungerle alla tabella ModuleIgnoreTable.

-   Aggiunta di una [tabella TextStyle](textstyle-table.md) non necessaria al modulo merge.

    Se il modulo merge non dispone di un'interfaccia utente (e in genere non lo è), è possibile eliminare la tabella in modo sicuro.

-   Aggiunta di voci non necessarie alla [tabella di directory](directory-table.md).

    Rimuovere le voci non necessarie dalla tabella directory.

-   Informazioni lasciate fuori dalla tabella di convalida del modulo di Unione \_ .

    In questo modo si impedisce la convalida del modulo merge. Aggiungere una \_ tabella di convalida completa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di interfacce utente nei moduli merge](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Creazione di tabelle di directory del modulo merge](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Convalida di moduli merge](validating-merge-modules.md)
</dt> </dl>

 

 



