---
title: File di intestazione
description: Il file di intestazione dell'interfaccia (Name. h) contiene le definizioni di tipo e le dichiarazioni di funzione basate sulla definizione dell'interfaccia nel file IDL corrente, nonché su tutti i tipi di dati e le operazioni dichiarati nei file inclusi con la direttiva \ include.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- file di intestazione MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ae80877b88d8061769b0d6bd56c13469427fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298627"
---
# <a name="the-header-files"></a><span data-ttu-id="96d43-104">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="96d43-104">The Header Files</span></span>

<span data-ttu-id="96d43-105">Il file di intestazione dell'interfaccia (Name. h) contiene le definizioni di tipo e le dichiarazioni di funzione basate sulla definizione dell'interfaccia nel file IDL corrente, nonché su tutti i tipi di dati e le operazioni dichiarati nei file inclusi con la \# direttiva include.</span><span class="sxs-lookup"><span data-stu-id="96d43-105">The interface header file (Name.h) contains type definitions and function declarations based on the interface definition in the current IDL file, as well as all the data types and operations declared in the files included with the \#include directive.</span></span> <span data-ttu-id="96d43-106">I tipi di dati dei file importati con la direttiva Import non vengono replicati nel file di intestazione. il file di intestazione generato contiene invece una riga di inclusione per il file H generato dal file importato.</span><span class="sxs-lookup"><span data-stu-id="96d43-106">Data types from the files imported with the import directive are not replicated to the header file; instead, the generated header file contains an include line to the H file generated from the imported file.</span></span>

<span data-ttu-id="96d43-107">Includere questo file nei file di origine per la DLL del proxy e per le applicazioni client che utilizzano l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="96d43-107">Include this file in the source files for the proxy DLL and for client applications that use the interface.</span></span>

<span data-ttu-id="96d43-108">Il nome predefinito per un file di intestazione generato da un file. idl è file. h.</span><span class="sxs-lookup"><span data-stu-id="96d43-108">The default name for a header file generated from a file.idl is File.h.</span></span> <span data-ttu-id="96d43-109">L'opzione del compilatore MIDL [**/header**](-header.md) esegue l'override del nome predefinito del file di intestazione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="96d43-109">The [**/header**](-header.md) MIDL compiler switch overrides the default name of the interface header file.</span></span>

 

 




