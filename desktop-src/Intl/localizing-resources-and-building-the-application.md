---
description: Questo argomento descrive come compilare una tipica applicazione MUI.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Localizzazione delle risorse e compilazione dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490fde8e0b6d9381b346409efad1501331be71d2d4e958be050274dc0428fe62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788501"
---
# <a name="localizing-resources-and-building-the-application"></a>Localizzazione delle risorse e compilazione dell'applicazione

Questo argomento descrive come compilare una tipica applicazione MUI. Si presuppone che si utilizzi un Microsoft Visual Studio per la scrittura del codice e Microsoft Visual Studio o la riga Visual Studio comando per la compilazione. Si presuppone di usare un file di soluzione con estensione sln per l'applicazione e di supportare un file Resource.h per riflettere il file di risorse della lingua di base.

> [!Note]  
> Se si usa Visual Studio riga di comando per la compilazione, si userà il **comando vcbuild** per compilare il file di soluzione.

 

I file dell'applicazione vengono compilati separatamente per ogni lingua. Ogni compilazione crea file .exe lingua e file .exe.mui specifici della lingua. Inoltre, diversi altri file vengono copiati nelle cartelle di rilascio appropriate.

La compilazione dell'applicazione dipende dal tipo di risorse e dal tipo di localizzazione in uso. Per la localizzazione pre-compilazione, si dispone di una copia del file della lingua di base localizzato per ogni lingua supportata. Per la localizzazione post-compilazione, è possibile copiare il file con estensione mui risultante dalla compilazione del file eseguibile e del modulo di risorse e fornire le copie ai localizzatori.

> [!Note]  
> Nella procedura seguente si presuppone che le risorse PE Win32 con Visual Studio progetto compilato per ogni linguaggio. Le risorse del linguaggio di base vengono fornite in un file RC e caricate usando un modulo DLL. È possibile ripetere la procedura in base alle esigenze per la compilazione per tutti i linguaggi supportati.

 

**Per compilare l'applicazione**

1.  Configurare un progetto Visual Studio per la lingua di base.
2.  Se si è interessati a usare un file di configurazione delle risorse con gli strumenti delle risorse, configurarne uno come descritto in Preparazione di un file [di configurazione delle risorse](preparing-a-resource-configuration-file.md).
3.  Impostare i parametri richiesti dall'utilità del compilatore RC nelle pagine delle proprietà per il progetto in Proprietà di **configurazione → risorse → riga** di comando → Opzioni aggiuntive .
4.  Eseguire il compilatore RC. L'utilità compila e suddivide le risorse non localizzabili e localizzabili in due file oggetto diversi, usando i dati di configurazione delle risorse. In questo passaggio le risorse indipendenti dalla lingua sono collegate in un file LN. Per altre informazioni, vedere la descrizione dell'utilità in [Utilità risorse](resource-utilities.md).
5.  Per collegare le risorse specifiche del linguaggio in un file con estensione mui specifico del linguaggio, impostare un evento di post-compilazione per il progetto nelle pagine delle proprietà in Proprietà di configurazione → Eventi di compilazione → Riga di comando dell'evento di **post-compilazione →**.
6.  Impostare un evento di post-compilazione per applicare il valore di checksum dal file LN al file con estensione mui per la lingua. Per questo passaggio è possibile usare l'utilità MUIRCT. Per altre informazioni, vedere la descrizione dell'utilità in [Utilità risorse](resource-utilities.md).
7.  Usare la riga di comando dell'evento di post-compilazione per aggiungere i comandi per copiare i file nella struttura di cartelle di rilascio appropriata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di interfaccia utente multilingue](using-multilingual-user-interface.md)
</dt> <dt>

[Preparazione di un file di configurazione delle risorse](preparing-a-resource-configuration-file.md)
</dt> <dt>

[Utilità per le risorse](resource-utilities.md)
</dt> </dl>

 

 



