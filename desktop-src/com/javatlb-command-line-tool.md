---
title: Strumento Command-Line JavaTLB
description: Strumento Command-Line JavaTLB
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0214648f7ad86613d6b35e3084021e2be24aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714428"
---
# <a name="javatlb-command-line-tool"></a><span data-ttu-id="eaaa1-103">Strumento Command-Line JavaTLB</span><span class="sxs-lookup"><span data-stu-id="eaaa1-103">JavaTLB Command-Line Tool</span></span>

<span data-ttu-id="eaaa1-104">JavaTLB è un componente di Visual J++ 5,0.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-104">JavaTLB is a component of Visual J++ 5.0.</span></span> <span data-ttu-id="eaaa1-105">JavaTLB è un'applicazione della riga di comando che genera file di classe per un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-105">JavaTLB is a command-line application that generates class files for a COM object.</span></span> <span data-ttu-id="eaaa1-106">I metodi che contengono tipi di dati che non possono essere rappresentati in modo accurato e sicuro in Java non vengono convertiti.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-106">Methods that contain data types that cannot be accurately and safely represented in Java are not converted.</span></span>

<span data-ttu-id="eaaa1-107">Diversamente dalla [procedura guidata libreria dei tipi Java](java-type-library-wizard.md), JavaTLB non genera un file di riepilogo contenente le informazioni sulla libreria dei tipi Java.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-107">Unlike the [Java Type Library Wizard](java-type-library-wizard.md), JavaTLB does not generate a summary file containing the Java type library information.</span></span>

<span data-ttu-id="eaaa1-108">Per generare file di classe Java per un singolo oggetto COM, dal prompt dei comandi eseguire:</span><span class="sxs-lookup"><span data-stu-id="eaaa1-108">To generate Java class files for a single COM object, from the command prompt run:</span></span>

<span data-ttu-id="eaaa1-109"> *nome file* JavaTLB</span><span class="sxs-lookup"><span data-stu-id="eaaa1-109">**javatlb** *filename*</span></span>

<span data-ttu-id="eaaa1-110">dove *filename* è il nome del file che contiene la libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-110">where *filename* is the name of the file that contains the type library.</span></span> <span data-ttu-id="eaaa1-111">Questo file può avere una delle seguenti estensioni di file:. tlb,. olb,. ocx,. dll o. exe.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-111">This file may have any of the following file name extensions: .tlb, .olb, .ocx, .dll, or .exe.</span></span>

<span data-ttu-id="eaaa1-112">Per generare file di classe Java per più oggetti COM, dal prompt dei comandi eseguire:</span><span class="sxs-lookup"><span data-stu-id="eaaa1-112">To generate Java class files for multiple COM objects, from the command prompt run:</span></span>

<span data-ttu-id="eaaa1-113">\**JavaTLB @ \* \* \* TextFile*</span><span class="sxs-lookup"><span data-stu-id="eaaa1-113">\**javatlb @\*\*\*TextFile*</span></span>

<span data-ttu-id="eaaa1-114">dove *TextFile* è il nome di un file di testo contenente un elenco dei file contenenti le librerie dei tipi dell'oggetto com.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-114">where *TextFile* is the name of a text file that contains a list of the files containing the COM object's type libraries.</span></span>

> [!Note]  
> <span data-ttu-id="eaaa1-115">In Visual J++ 6,0 lo strumento da riga di comando JavaTLB viene sostituito dallo [strumento JActiveX](jactivex-command-line-tool.md).</span><span class="sxs-lookup"><span data-stu-id="eaaa1-115">In Visual J++ 6.0, the JavaTLB command-line tool is replaced by the [JActiveX tool](jactivex-command-line-tool.md).</span></span> <span data-ttu-id="eaaa1-116">Per ulteriori informazioni, vedere la documentazione di Visual J++ 6,0.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-116">For more information, see the Visual J++ 6.0 documentation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eaaa1-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eaaa1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaaa1-118">Conversione in Java</span><span class="sxs-lookup"><span data-stu-id="eaaa1-118">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




