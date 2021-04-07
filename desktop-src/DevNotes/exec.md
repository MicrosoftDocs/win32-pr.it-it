---
description: HKLM \\ software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748759"
---
# <a name="exec"></a><span data-ttu-id="cdfe3-103">Exec</span><span class="sxs-lookup"><span data-stu-id="cdfe3-103">Exec</span></span>

<span data-ttu-id="cdfe3-104">**HKLM \\ software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**</span><span class="sxs-lookup"><span data-stu-id="cdfe3-104">**HKLM\\Software\\Microsoft\\Internet Explorer\\Extensions\\{e2e2dd38-d088-4134-82b7-f2ba38496583}**</span></span>



| <span data-ttu-id="cdfe3-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cdfe3-105">Data type</span></span> | <span data-ttu-id="cdfe3-106">Range</span><span class="sxs-lookup"><span data-stu-id="cdfe3-106">Range</span></span>                    | <span data-ttu-id="cdfe3-107">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="cdfe3-107">Default value</span></span> |
|-----------|--------------------------|---------------|
| <span data-ttu-id="cdfe3-108">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="cdfe3-108">REG\_SZ</span></span>   | <span data-ttu-id="cdfe3-109">*Percorso del file eseguibile*</span><span class="sxs-lookup"><span data-stu-id="cdfe3-109">*Path to the executable*</span></span> |               |



 

## <a name="browser-integration-steps"></a><span data-ttu-id="cdfe3-110">Passaggi di integrazione del browser</span><span class="sxs-lookup"><span data-stu-id="cdfe3-110">Browser Integration Steps</span></span>

1.  <span data-ttu-id="cdfe3-111">Usare la funzione [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) per determinare se la diagnostica di rete è installata.</span><span class="sxs-lookup"><span data-stu-id="cdfe3-111">Use the [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) function to determine whether the Network Diagnostic is installed.</span></span> <span data-ttu-id="cdfe3-112">Se è installato, la chiave **{e2e2dd38-d088-4134-82b7-f2ba38496583}** è presente.</span><span class="sxs-lookup"><span data-stu-id="cdfe3-112">If it is installed, the **{e2e2dd38-d088-4134-82b7-f2ba38496583}** key is present.</span></span>
2.  <span data-ttu-id="cdfe3-113">Usare la funzione [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) per recuperare il percorso del file eseguibile di diagnostica di rete dalla voce **Exec** .</span><span class="sxs-lookup"><span data-stu-id="cdfe3-113">Use the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to retrieve the path of the Network Diagnostic executable file from the **Exec** entry.</span></span>
3.  <span data-ttu-id="cdfe3-114">Visualizza la pagina nuovo errore se la diagnostica è installata nel sistema.</span><span class="sxs-lookup"><span data-stu-id="cdfe3-114">Display the new error page if the diagnostic is installed on the system.</span></span>
4.  <span data-ttu-id="cdfe3-115">Creare un'estensione del browser che crei una voce della barra degli strumenti standard se la diagnostica è installata nel sistema.</span><span class="sxs-lookup"><span data-stu-id="cdfe3-115">Create a browser extension that creates a standard toolbar item if the diagnostic is installed on the system.</span></span>
5.  <span data-ttu-id="cdfe3-116">Eseguire l'eseguibile di diagnostica di rete usando il percorso recuperato nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="cdfe3-116">Execute the Network Diagnostic executable using the path retrieved in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdfe3-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cdfe3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdfe3-118">Panoramica delle funzionalità degli strumenti di diagnostica di rete</span><span class="sxs-lookup"><span data-stu-id="cdfe3-118">Network Diagnostics Tools Feature Overview</span></span>](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
