---
description: ICEM13 verifica che il modulo merge non contenga gli assembly di configurazione e i criteri del server di pubblicazione.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286906cf162f24dce7105835544c3a387993ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881049"
---
# <a name="icem13"></a><span data-ttu-id="5b954-103">ICEM13</span><span class="sxs-lookup"><span data-stu-id="5b954-103">ICEM13</span></span>

<span data-ttu-id="5b954-104">ICEM13 verifica che il modulo merge non contenga gli assembly di configurazione e i criteri del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="5b954-104">ICEM13 verifies that the merge module does not contain publisher policy and configuration assemblies.</span></span> <span data-ttu-id="5b954-105">I criteri e gli assembly di configurazione del server di pubblicazione non devono essere inclusi nei moduli unione destinati alla ridistribuzione perché possono influire su altre applicazioni nel computer di un utente.</span><span class="sxs-lookup"><span data-stu-id="5b954-105">Publisher policy and configuration assemblies should not be included in merge modules intended for redistribution because this can affect other applications on a user's computer.</span></span>

<span data-ttu-id="5b954-106">Questo ICEM è disponibile nel file Mergemod. cub fornito in Windows Installer SDK 2,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5b954-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="5b954-107">Per informazioni dettagliate, vedere [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="5b954-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="5b954-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="5b954-108">Result</span></span>

<span data-ttu-id="5b954-109">ICEM13 Invia un messaggio di avviso se trova un componente specificato nel campo componente della [tabella MsiAssembly](msiassembly-table.md) del modulo merge, ovvero un criterio editore o un assembly di configurazione.</span><span class="sxs-lookup"><span data-stu-id="5b954-109">ICEM13 posts a warning message if it finds a component specified in the Component field of the merge module's [MsiAssembly Table](msiassembly-table.md) that is a publisher policy or configuration assembly.</span></span>

## <a name="example"></a><span data-ttu-id="5b954-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="5b954-110">Example</span></span>

<span data-ttu-id="5b954-111">ICEM13 invia il seguente messaggio di avviso se trova una riga nella [tabella MsiAssembly](msiassembly-table.md) con un componente " \[ 1 \] " specificato nel campo componente, ovvero un criterio editore o un assembly di configurazione che è stato incluso nel modulo unione.</span><span class="sxs-lookup"><span data-stu-id="5b954-111">ICEM13 posts the following warning message if it finds a row in the [MsiAssembly Table](msiassembly-table.md) with a component '\[1\]' specified in the Component field that is a publisher policy or configuration assembly that has been included in the merge module.</span></span>

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

<span data-ttu-id="5b954-112">È possibile installare i criteri editore e gli assembly di configurazione utilizzando la Windows Installer, non è consigliabile ridistribuire questi assembly nei moduli unione.</span><span class="sxs-lookup"><span data-stu-id="5b954-112">It is possible to install publisher policy and configuration assemblies using the Windows Installer, it is not recommended that these assemblies be redistributed in merge modules.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b954-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b954-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b954-114">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="5b954-114">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



