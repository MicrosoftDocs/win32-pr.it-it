---
title: Panoramica di StoClien
description: L'esempio StoClien illustra come il client usa l'archiviazione strutturata e come indirizza un componente server a usare questa risorsa di archiviazione.
ms.assetid: 1f540e0f-2189-4f45-aad3-9b4b56732907
keywords:
- Panoramica di StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee37f6f84cf981bda637abbd96ff8e8f0314d8ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297755"
---
# <a name="stoclien-overview"></a>Panoramica di StoClien

## <a name="purpose"></a>Scopo

L'obiettivo principale dell'esempio [StoClien](structured-storage-client-sample--stoclien-.md) è il modo in cui il client usa l'archiviazione strutturata e come indica a un componente server di usare questa risorsa di archiviazione. L'esempio StoClien illustra un modello di programmazione di servizi di archiviazione strutturati.

## <a name="functionality"></a>Funzionalità

La funzionalità [StoClien](structured-storage-client-sample--stoclien-.md) è simile a quella degli esempi "Scribble" in alcune versioni di Microsoft Visual C++. La differenza tra l'esempio StoClien e l'esempio [StoServe](structured-storage-server-sample--stoserve-.md) è un'architettura interna basata sulla tecnologia com. Una chiara distinzione architetturale viene mantenuta tra client COM e server COM.

[StoClien](structured-storage-client-sample--stoclien-.md) carica e salva i relativi disegni nell'archivio strutturato dei file composti com.

L'esempio [StoClien](structured-storage-client-sample--stoclien-.md) crea e usa l'oggetto com della cocarta collegabile fornito come \_ componente DllPaper CLSID nel server [StoServe](structured-storage-server-sample--stoserve-.md) . Il client StoClien crea un oggetto Copaper e lo controlla tramite l'interfaccia IPaper esposta dall'oggetto. StoClien ottiene i dati di disegno dall'utente e li rappresenta graficamente in una finestra gestita. StoClien usa l'interfaccia IPaper di Copaper per salvare i dati di disegno in un documento e per indirizzare le operazioni di archiviazione file su questi dati.

Un oggetto COM di cocarta incapsula solo l'archiviazione basata su server dei dati della carta di disegno: non viene fornito alcun comportamento dell'interfaccia utente grafica (GUI) sul lato server. Tutto il comportamento dell'interfaccia utente grafica è isolato nel client. Le funzionalità di gestione e archiviazione dei dati degli oggetti di un documento sono disponibili solo tramite un'interfaccia personalizzata COM, IPaper.

[StoClien](structured-storage-client-sample--stoclien-.md) coopera con il Copaper per caricare e salvare i dati di disegno del documento. StoClien ottiene un'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) per l'oggetto di archiviazione in un file composto. Nelle operazioni di caricamento e salvataggio, StoClien passa un puntatore all'interfaccia **IStorage** per la cocarta nel server. Il Copaper usa il **IStorage** fornito per creare flussi nell'archiviazione. Un documento può quindi usare l'interfaccia [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) standard per la lettura e la scrittura dei dati di disegno gestiti.

Il Copaper gestisce solo i dati di disegno; non esegue alcuna azione GUI. [StoClien](structured-storage-client-sample--stoclien-.md) fornisce l'interfaccia utente grafica per l'applicazione di disegno. Incapsula questo oggetto in un oggetto C++ CGuiPaper centrale.

[StoClien](structured-storage-client-sample--stoclien-.md) implementa anche l'interfaccia IPaperSink personalizzata in un oggetto com COPaperSink e connette questa interfaccia a un punto di connessione appropriato nell'oggetto della cocarta del server. Il Copaper usa l'interfaccia IPaperSink connessa per inviare le notifiche a StoClien. Il ridisegno della GUI normale dei dati di disegno della cocarta viene eseguito in StoClien usando la tecnologia di oggetti collegabile per la stampa.

[StoClien](structured-storage-client-sample--stoclien-.md) è un'applicazione che è possibile eseguire direttamente nel modo normale o dalla finestra del prompt dei comandi. StoClien accetta un parametro di nome file facoltativo nella riga di comando.

Nell'esempio seguente Drawing. PAP è un file composto che contiene l'archiviazione strutturata compatibile con DllPaper di dati del disegno. Se non viene specificato alcun parametro del nome file della riga di comando, [StoClien](structured-storage-client-sample--stoclien-.md) usa il nome file predefinito StoClien. PAP e tenta di aprirlo nella stessa directory del Stoclien.exe in esecuzione.

**StoClien c: \\ \\ Drawings Drawing. pap**

## <a name="support-information"></a>Informazioni relative al supporto

Per ulteriori informazioni, descrizioni funzionali e un'esercitazione sul codice per [StoClien](structured-storage-client-sample--stoclien-.md), vedere la sezione relativa alla presentazione del codice in Stoclien.htm. Per ulteriori informazioni sul funzionamento dell'utente esterno di StoClien, vedere le sezioni utilizzo e operazione in Stoclien.htm. Per leggere Stoclient.htm, eseguire Tutorial.exe nella directory Main tutorial e fare clic sulla lezione StoClien nella tabella lessons. In alternativa, fare clic su Stoclien.htm dopo aver individuato la directory principale dell'esercitazione in Esplora risorse. Per ulteriori informazioni sul funzionamento di [**StoServe**](structured-storage-server-sample--stoserve-.md) ed espone i servizi a StoClien, vedere Stoserve.htm nella directory principale dell'esercitazione. Tenere presente che è necessario compilare il Stoserve.dll prima di compilare StoClien. Il makefile per [**StoServe**](structured-storage-server-sample--stoserve-.md) registra il server nel registro di sistema, pertanto è necessario compilare [**StoServe**](structured-storage-server-sample--stoserve-.md) prima di provare a eseguire StoClien.

Per ulteriori informazioni sulla configurazione di un sistema per compilare e testare gli esempi di codice in questa serie di esercitazioni COM, vedere [How to Build Samples](how-to-build-samples.md). Il Makefile fornito è compatibile con Microsoft NMAKE. Per creare una build di debug, eseguire il comando NMAKE nella finestra del prompt dei comandi.

Per praticità, viene fornito un file di progetto per ogni esempio da utilizzare in Microsoft Visual Studio. Per caricare il progetto per l'esempio [StoClien](structured-storage-client-sample--stoclien-.md) , eseguire Visual Studio al prompt dei comandi nella directory di esempio come indicato di seguito:

STOCLIEN MSDEV. DSP

È anche possibile fare doppio clic sul file Stoclient. DSP in Esplora risorse per caricare un progetto di esempio in Visual Studio. In Visual Studio è possibile esplorare le classi C++ dell'origine di esempio e in genere eseguire le altre operazioni di modifica-compilazione-debug. Tenere presente che, nell'ambito dell'SDK del server, la compilazione di questi esempi da Visual Studio richiede l'impostazione appropriata dei percorsi di directory in Visual Studio. Per ulteriori informazioni, vedere [How to Build Samples](how-to-build-samples.md).

## <a name="remarks"></a>Commenti

Prima di poter eseguire il client, è necessario compilare l'esempio client e altri esempi correlati. Per ulteriori informazioni sulla compilazione degli esempi, vedere [How to Build Samples](how-to-build-samples.md). Se sono stati compilati gli esempi appropriati, Stoclien.exe è l'eseguibile del client da eseguire per questo esempio.

L'applicazione Stoclien.exe fornisce l'interfaccia utente per questa esercitazione. Viene esercitato il Stoserve.dll associato, ma indipendente, per illustrare l'utilizzo del client e del server dell'archiviazione strutturata COM nei file composti.

 

 




