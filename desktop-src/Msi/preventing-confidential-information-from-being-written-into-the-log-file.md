---
description: Gli sviluppatori possono impedire l'immissione di informazioni riservate, ad esempio password, nel file di log durante un'installazione Windows Installer.
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: Prevenzione della scrittura di informazioni riservate nel file di log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049896"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a><span data-ttu-id="6ad68-103">Prevenzione della scrittura di informazioni riservate nel file di log</span><span class="sxs-lookup"><span data-stu-id="6ad68-103">Preventing Confidential Information from Being Written into the Log File</span></span>

<span data-ttu-id="6ad68-104">Quando si usa la Windows Installer, è possibile impedire l'immissione nel file di log di informazioni riservate, ad esempio le password, e renderle visibili.</span><span class="sxs-lookup"><span data-stu-id="6ad68-104">When using the Windows Installer, you can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span>

-   <span data-ttu-id="6ad68-105">Il programma di installazione non scrive mai le informazioni nella colonna password della [tabella ServiceInstall](serviceinstall-table.md) nel log.</span><span class="sxs-lookup"><span data-stu-id="6ad68-105">The Installer never writes the information in the Password column of the [ServiceInstall table](serviceinstall-table.md) into the log.</span></span>
-   <span data-ttu-id="6ad68-106">È possibile impedire al programma di installazione di scrivere la proprietà associata a un [controllo di modifica](edit-control.md) nel log impostando l' [attributo di controllo delle password](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="6ad68-106">You can prevent the Installer from writing the property that is associated with an [Edit Control](edit-control.md) into the log by setting the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="6ad68-107">La proprietà associata a un controllo di modifica con l'attributo di controllo password è nascosta anche se i criteri di [debug](debug.md) sono impostati su un valore pari a 7.</span><span class="sxs-lookup"><span data-stu-id="6ad68-107">The property associated with an Edit Control that has the Password Control Attribute is hidden even if the [Debug](debug.md) policy is set to a value of 7.</span></span>
-   <span data-ttu-id="6ad68-108">È possibile impedire al programma di installazione di scrivere una proprietà privata nel log includendo la proprietà nella proprietà [**MsiHiddenProperties**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="6ad68-108">You can prevent the Installer from writing a private property into the log by including the property in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>
    > [!Note]  
    > <span data-ttu-id="6ad68-109">Questo metodo consente di rendere visibili le informazioni riservate in una riga di comando nel log.</span><span class="sxs-lookup"><span data-stu-id="6ad68-109">This method can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="6ad68-110">Quando il criterio di [debug](debug.md) è impostato su un valore pari a 7, il programma di installazione scriverà le informazioni immesse in una riga di comando nel log.</span><span class="sxs-lookup"><span data-stu-id="6ad68-110">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="6ad68-111">In questo modo la proprietà immessa in una riga di comando è visibile anche se la proprietà è inclusa nella proprietà [**MsiHiddenProperties**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="6ad68-111">This makes the property entered on a command line visible even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>

     

-   <span data-ttu-id="6ad68-112">È possibile impedire che le informazioni nella colonna di destinazione della tabella [CustomAction](customaction-table.md) vengano scritte nel log includendo il flag di bit HideTarget nel campo Type della tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="6ad68-112">You can prevent the information in the Target column of the [CustomAction](customaction-table.md) Table from being written into the log by including the HideTarget bit flag in the Type field of the CustomAction table.</span></span> <span data-ttu-id="6ad68-113">Il valore di questo flag è 8192 (0x2000).</span><span class="sxs-lookup"><span data-stu-id="6ad68-113">The value of this flag is 8192 (0x2000).</span></span> <span data-ttu-id="6ad68-114">Per altre informazioni, vedere [opzione di destinazione nascosta dell'azione personalizzata](custom-action-hidden-target-option.md).</span><span class="sxs-lookup"><span data-stu-id="6ad68-114">For more information, see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

 

 



