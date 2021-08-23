---
title: Panoramica di StoClien
description: L'esempio StoClien illustra come il client usa l'archiviazione strutturata e come indirizza un componente server all'uso di questa archiviazione.
ms.assetid: 1f540e0f-2189-4f45-aad3-9b4b56732907
keywords:
- Panoramica di StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a28c8d0f4740b5a1d5f93934fb055d16e2ed9d843bcb11b210e6cde9589d53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661851"
---
# <a name="stoclien-overview"></a>Panoramica di StoClien

## <a name="purpose"></a>Scopo

L'obiettivo principale dell'esempio [StoClien](structured-storage-client-sample--stoclien-.md) è il modo in cui il client usa l'archiviazione strutturata e indica a un componente server di usare questa archiviazione. L'esempio StoClien illustra un modello di programmazione dei servizi di archiviazione strutturata.

## <a name="functionality"></a>Funzionalità

La [funzionalità StoClien](structured-storage-client-sample--stoclien-.md) è simile agli esempi "scribble" in alcune versioni di Microsoft Visual C++. La differenza tra l'esempio StoClien e l'esempio [StoServe](structured-storage-server-sample--stoserve-.md) è un'architettura interna basata sulla tecnologia COM. Viene mantenuta una netta distinzione dell'architettura tra client COM e server COM.

[StoClien](structured-storage-client-sample--stoclien-.md) carica e salva i disegni nell'archiviazione strutturata dei file composti COM.

[L'esempio StoClien](structured-storage-client-sample--stoclien-.md) crea e usa l'oggetto COM COPaper collegabile fornito come componente \_ CLSID DllPaper nel server [StoServe.](structured-storage-server-sample--stoserve-.md) Il client StoClien crea un oggetto COPaper e lo controlla tramite l'interfaccia IPaper esponga l'oggetto. StoClien ottiene i dati di disegno dall'utente e la rappresenta graficamente in una finestra che gestisce. StoClien usa l'interfaccia COPaper IPaper per salvare i dati di disegno in COPaper e indirizzare le operazioni di archiviazione dei file su questi dati.

Un oggetto COM COPaper incapsula solo l'archiviazione basata su server dei dati della carta di disegno: sul lato server non viene fornito alcun comportamento dell'interfaccia utente grafica (GUI). Tutto il comportamento dell'interfaccia utente grafica è isolato nel client. Le funzionalità di gestione dei dati e archiviazione degli oggetti COPaper sono disponibili solo tramite un'interfaccia personalizzata COM, IPaper.

[StoClien collabora](structured-storage-client-sample--stoclien-.md) con COPaper per caricare e salvare i dati di disegno di COPaper. StoClien ottiene [**un'interfaccia IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) per l'oggetto di archiviazione in un file composto. Nelle operazioni di caricamento e salvataggio StoClien passa un puntatore **all'interfaccia IStorage** a COPaper nel server. COPaper usa **l'oggetto IStorage** fornito per creare flussi nell'archiviazione. COPaper può quindi usare [**l'interfaccia IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) standard per la lettura e la scrittura dei dati di disegno gestiti.

COPaper gestisce solo i dati di disegno. non esegue azioni GUI. [StoClien fornisce](structured-storage-client-sample--stoclien-.md) l'interfaccia utente grafica per l'applicazione di disegno. Incapsula questo oggetto in un oggetto CGuiPaper C++ centrale.

[StoClien](structured-storage-client-sample--stoclien-.md) implementa anche l'interfaccia IPaperSink personalizzata in un oggetto COM COPaperSink e connette questa interfaccia a un punto di connessione appropriato nell'oggetto COPaper del server. COPaper usa l'interfaccia IPaperSink connessa per inviare notifiche a StoClien. Il normale ridisegno dell'interfaccia utente grafica dei dati di disegno DI COPaper viene eseguito in StoClien usando la tecnologia degli oggetti collegabili COPaper.

[StoClien](structured-storage-client-sample--stoclien-.md) è un'applicazione che è possibile eseguire direttamente nel modo normale o dalla finestra del prompt dei comandi. StoClien accetta un parametro di nome file facoltativo nella riga di comando.

Nell'esempio seguente Drawing.pap è un file composto contenente l'archiviazione strutturata dei dati di disegno compatibile con DllPaper. Se non viene specificato alcun parametro di nome file della riga di comando, [StoClien](structured-storage-client-sample--stoclien-.md) usa il nome file predefinito Stoclien.pap e tenta di aprirlo nella stessa directory del file di Stoclien.exe.

**StoClien c: \\ drawings \\ drawing.pap**

## <a name="support-information"></a>Informazioni relative al supporto

Per altre informazioni, descrizioni funzionali e un'esercitazione sul codice per [StoClien,](structured-storage-client-sample--stoclien-.md)vedere la sezione Code Tour in Stoclien.htm. Per altre informazioni sul funzionamento degli utenti esterni di StoClien, vedere le sezioni Utilizzo e operazione in Stoclien.htm. Per leggere Stoclient.htm, eseguire Tutorial.exe nella directory principale dell'esercitazione e fare clic sulla lezione StoClien nella tabella delle lezioni. In alternativa, fare clic Stoclien.htm dopo aver individuato la directory principale dell'esercitazione in Windows Explorer. Per altre informazioni sul funzionamento [**di StoServe**](structured-storage-server-sample--stoserve-.md) ed espone i relativi servizi a StoClien, vedere Stoserve.htm nella directory principale dell'esercitazione. Tenere presente che è necessario compilare il Stoserve.dll prima di compilare StoClien. Il makefile per [**StoServe**](structured-storage-server-sample--stoserve-.md) registra il server nel Registro di sistema, quindi è necessario compilare [**StoServe**](structured-storage-server-sample--stoserve-.md) prima di provare a eseguire StoClien.

Per altre informazioni sulla configurazione di un sistema per compilare e testare gli esempi di codice in questa serie di esercitazioni COM, vedere [How to Build Samples](how-to-build-samples.md). Il makefile fornito (MAKEFILE) è compatibile con Microsoft NMAKE. Per creare una build di debug, eseguire il comando NMAKE nella finestra del prompt dei comandi.

Per praticità, viene fornito un file di progetto per ogni esempio da usare in Microsoft Visual Studio. Per caricare il progetto per l'esempio [StoClien,](structured-storage-client-sample--stoclien-.md) eseguire Visual Studio al prompt dei comandi nella directory di esempio come segue:

MSDEV STOCLIEN. Dsp

È anche possibile fare doppio clic sul file Stoclient.dsp in Windows Explorer per caricare un progetto di esempio in Visual Studio. In Visual Studio, è possibile esplorare le classi C++ dell'origine di esempio ed eseguire in genere le altre operazioni edit-compile-debug. Tenere presente che, come parte di Server SDK, la compilazione di questi esempi dall'interno di Visual Studio richiede l'impostazione corretta dei percorsi di directory in Visual Studio. Per altre informazioni, vedere [Come compilare gli esempi](how-to-build-samples.md).

## <a name="remarks"></a>Commenti

Prima di poter eseguire il client, è necessario compilare l'esempio client e altri esempi correlati. Per altre informazioni sulla compilazione degli esempi, vedere [Come compilare gli esempi](how-to-build-samples.md). Se sono stati compilati gli esempi appropriati, Stoclien.exe è l'eseguibile client da eseguire per questo esempio.

LStoclien.exe appalto fornisce l'interfaccia utente per questa esercitazione. Esercita l'oggetto associato, ma indipendente, Stoserve.dll per illustrare l'uso sia client che server dell'archiviazione strutturata COM nei file composti.

 

 




