---
title: Compilazione dell'applicazione di esempio tramite Visual Studio
description: Compilazione dell'applicazione di esempio tramite Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Windows Gestione dispositivi multimediali, esempi
- Gestione dispositivi, esempi
- applicazioni desktop, esempi
- Windows Media Device Manager, esempio di applicazione desktop
- Gestione dispositivi, esempio di applicazione desktop
- esempi, applicazioni desktop
- esempi, compilazione con Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8b32cd5931a88bc41b8eee7171b6ab4ab18b629a8108007d68094180efaa77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586252"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a>Compilazione dell'applicazione di esempio tramite Visual Studio

L Windows SDK di Gestione dispositivi multimediali Visual Studio una soluzione compatibile con Microsoft Visual Studio 2005.

Prima di compilare l'applicazione di esempio, è necessario rinominare il file di intestazione shtypes.h per evitare conflitti con un file con lo stesso nome disponibile in Microsoft Platform SDK. Ad esempio, è possibile rinominare <*SDK Installation Path* > \\ WMFSDK11 include \\ \\ shtypes.h in <SDK Installation *Path* > \\ WMFSDK11 \\ include \\ shtypes.h.backup.

Per compilare l'applicazione, avviare un'istanza di Visual Studio 2005, aprire il file di soluzione wmdmapp.sln, disponibile nella cartella percorso di installazione *dell'SDK*<> \\ WMFSDK11 apps wmdmapp e scegliere l'opzione \\ \\ **Compila/Compila** soluzione. Verranno creati due file di progetto: il progetto helper, proghelp.vcproj, nonché l'applicazione principale wmdmapp.vcproj. Inoltre, creerà la DLL helper di stato e l'applicazione principale (WMDMApp.exe).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Applicazione desktop di esempio**](sample-desktop-application.md)
</dt> </dl>

 

 




