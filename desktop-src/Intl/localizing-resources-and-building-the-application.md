---
description: Questo argomento descrive come compilare una tipica applicazione MUI.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Localizzazione delle risorse e compilazione dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308704"
---
# <a name="localizing-resources-and-building-the-application"></a>Localizzazione delle risorse e compilazione dell'applicazione

Questo argomento descrive come compilare una tipica applicazione MUI. Si presuppone che si stiano usando Microsoft Visual Studio per la codifica e Microsoft Visual Studio o la riga di comando di Visual Studio per la compilazione. Si presuppone l'utilizzo di un file di soluzione con estensione sln per l'applicazione e il supporto di un file Resource. h per riflettere il file di risorse della lingua di base.

> [!Note]  
> Se si usa la riga di comando di Visual Studio per la compilazione, si userà il comando **VCBuild** per compilare il file di soluzione.

 

I file dell'applicazione vengono compilati separatamente per ogni lingua. Ogni compilazione crea file con estensione exe, indipendenti dalla lingua e file. exe. mui specifici della lingua. Inoltre, diversi altri file vengono copiati nelle cartelle della versione appropriate.

La compilazione dell'applicazione dipende dal tipo di risorse e dal tipo di localizzazione utilizzato. Per la localizzazione pre-compilazione, è presente una copia del file della lingua di base localizzata per ogni lingua supportata. Per la localizzazione post-compilazione, è possibile copiare il file con estensione MUI risultante dalla compilazione del modulo eseguibile e risorse e fornire le copie ai localizzatori.

> [!Note]  
> Nella procedura seguente si presuppone che le risorse PE Win32 con un progetto di Visual Studio siano compilate per ogni lingua. Le risorse della lingua di base vengono fornite in un file RC e caricate tramite un modulo DLL. È possibile ripetere la procedura in base alle esigenze per la compilazione per tutte le lingue supportate.

 

**Per compilare l'applicazione**

1.  Configurare un progetto di Visual Studio per la lingua di base.
2.  Se si è interessati all'uso di un file di configurazione delle risorse con gli strumenti di risorse, impostarne uno come descritto in [preparazione di un file di configurazione delle risorse](preparing-a-resource-configuration-file.md).
3.  Impostare i parametri richiesti dall'utilità del compilatore RC nelle pagine delle proprietà del progetto in **proprietà di configurazione → risorse → riga di comando → opzioni aggiuntive**.
4.  Eseguire il compilatore RC. L'utilità compila e suddivide le risorse non localizzabili e localizzabili in due file oggetto diversi, usando i dati di configurazione delle risorse. In questo passaggio le risorse indipendenti dalla lingua sono collegate a un file in. Per ulteriori informazioni, vedere la descrizione dell'utilità in [Utilità risorse](resource-utilities.md).
5.  Per collegare le risorse specifiche della lingua in un file con estensione MUI specifico della lingua, impostare un evento di post-compilazione per il progetto nelle pagine delle proprietà in **proprietà di configurazione → eventi di compilazione → evento post-compilazione → riga di comando**.
6.  Impostare un evento di post-compilazione per applicare il valore di checksum dal file LN al file con estensione MUI per la lingua. È possibile usare l'utilità MUIRCT per questo passaggio. Per ulteriori informazioni, vedere la descrizione dell'utilità in [Utilità risorse](resource-utilities.md).
7.  Utilizzare la riga di comando eventi post-compilazione per aggiungere comandi per copiare i file nella struttura di cartelle della versione appropriata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'interfaccia utente multilingue](using-multilingual-user-interface.md)
</dt> <dt>

[Preparazione di un file di configurazione delle risorse](preparing-a-resource-configuration-file.md)
</dt> <dt>

[Utilità per le risorse](resource-utilities.md)
</dt> </dl>

 

 



