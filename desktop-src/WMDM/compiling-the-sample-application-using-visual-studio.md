---
title: Compilazione dell'applicazione di esempio con Visual Studio
description: Compilazione dell'applicazione di esempio con Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Windows Media Gestione dispositivi, esempi
- Gestione dispositivi, esempi
- applicazioni desktop, esempi
- Windows Media Gestione dispositivi, esempio di applicazione desktop
- Esempio di Gestione dispositivi, applicazione desktop
- esempi, applicazioni desktop
- esempi, compilazione con Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf47f7a45ad17711145df810926fafb0f2aedcec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044484"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a>Compilazione dell'applicazione di esempio con Visual Studio

Windows Media Gestione dispositivi SDK include una soluzione di Visual Studio compatibile con Microsoft Visual Studio 2005.

Prima di compilare l'applicazione di esempio, è necessario rinominare il file di intestazione shtypes. h per evitare conflitti con un file con lo stesso nome trovato in Microsoft Platform SDK. Ad esempio, è possibile rinominare il *percorso di installazione di <SDK* > \\ WMFSDK11 \\ includere \\ shtypes. h nel percorso di installazione di <*SDK* > \\ WMFSDK11 \\ includere \\ shtypes. h. backup.

Per compilare l'applicazione, avviare un'istanza di Visual Studio 2005, aprire il file di soluzione WMDMApp. sln, disponibile nella cartella <*percorso di installazione SDK* > \\ WMFSDK11 \\ Apps \\ WMDMApp e scegliere l'opzione **Compila/Compila soluzione** . In questo modo vengono creati due file di progetto: il progetto helper, proghelp. vcproj, e l'applicazione principale WMDMApp. vcproj. Inoltre, creerà la DLL dell'helper di avanzamento e l'applicazione principale (WMDMApp.exe).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Applicazione desktop di esempio**](sample-desktop-application.md)
</dt> </dl>

 

 




