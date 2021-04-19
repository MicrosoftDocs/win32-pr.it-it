---
description: Creazione di pacchetti di installazione per applicazioni COM+
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Creazione di pacchetti di installazione per applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ec34852ab405d965fa1ad8f8fb5892616d1347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304829"
---
# <a name="creating-installation-packages-for-com-applications"></a>Creazione di pacchetti di installazione per applicazioni COM+

È possibile utilizzare lo strumento di amministrazione Servizi componenti o la libreria di amministrazione COM+ per creare pacchetti di installazione per applicazioni COM+ e proxy di applicazione.

COM+ genera Windows Installer pacchetti di installazione, che in un singolo file contengono tutti i componenti necessari per installare un'applicazione COM+ in un altro computer.

Quando si esporta un'applicazione COM+, lo strumento di amministrazione Servizi componenti determina il set di classi, i componenti e gli attributi dell'applicazione, nonché gli attributi a livello di applicazione. Da queste informazioni, lo strumento di amministrazione Servizi componenti genera un singolo file con estensione msi, che contiene quanto segue:

-   Windows Installer tabelle con le informazioni di registrazione COM (vedere la documentazione Windows Installer per informazioni dettagliate).
-   Un file con estensione APL contenente gli attributi dell'applicazione. Si tratta di un file interno. il formato del file non è documentato.
-   Dll e librerie dei tipi che descrivono le interfacce implementate dalle classi dell'applicazione COM+.

Oltre al file con estensione msi, lo strumento di amministrazione Servizi componenti genera un file CAB. Questo file esegue il wrapping del file con estensione msi, consentendo allo sviluppatore di distribuire l'applicazione COM+ tramite Microsoft Internet Explorer.

> [!Note]  
> Quando si esporta un'applicazione COM+, lo strumento di amministrazione Servizi componenti esegue il pacchetto solo delle parti COM+ standard dell'applicazione. Non esegue il pacchetto, ad esempio, di eventuali file di dati o DLL dipendenti. Prima di installare l'applicazione COM+, è necessario che i file DLL dipendenti siano installati in un computer. In alternativa, è possibile utilizzare lo strumento di creazione Windows Installer per aggiungere questi file dipendenti al file con estensione msi generato dallo strumento di amministrazione Servizi componenti. Per informazioni dettagliate, vedere la documentazione Windows Installer.

 

## <a name="installing-com-applications-on-other-computers"></a>Installazione di applicazioni COM+ in altri computer

Il file di Windows Installer (MSI) generato dallo strumento di amministrazione Servizi componenti può essere utilizzato per installare l'applicazione COM+ in un altro computer. Il file con estensione msi contenente un'applicazione COM+ può essere installato solo su computer che supportano servizi COM+. Per le procedure dettagliate relative alla distribuzione di applicazioni COM+, vedere "installazione di applicazioni COM+" nella Guida all'amministrazione di Servizi componenti.

A meno che il file con estensione msi non venga modificato utilizzando uno strumento di creazione Windows Installer, le applicazioni COM+ installate utilizzando il Windows Installer vengono visualizzate nel pannello di controllo Installazione applicazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Distribuzione di proxy di applicazione](deploying-application-proxies.md)
</dt> <dt>

[Catalogo COM+](the-com--catalog.md)
</dt> </dl>

 

 



