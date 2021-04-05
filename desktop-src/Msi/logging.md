---
description: Questo criterio di sistema per computer viene usato solo se la registrazione non è stata abilitata dall' \# opzione della riga di comando &0034;/l&\# 0034; o da MsiEnableLog.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Registrazione (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756614"
---
# <a name="logging-windows-installer"></a><span data-ttu-id="2ffff-103">Registrazione (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="2ffff-103">Logging (Windows Installer)</span></span>

<span data-ttu-id="2ffff-104">Questo [criterio di sistema](system-policy.md) per computer viene usato solo se la registrazione non è stata abilitata dall'opzione della riga di comando "/l" o da [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga).</span><span class="sxs-lookup"><span data-stu-id="2ffff-104">This per-machine [system policy](system-policy.md) is used only if logging has not been enabled by the "/L" command line option or by [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga).</span></span> <span data-ttu-id="2ffff-105">Se il criterio è impostato in questo caso, il programma di installazione crea un file di log in% Temp% con il nome casuale: MSI \* . LOG.</span><span class="sxs-lookup"><span data-stu-id="2ffff-105">If the policy is set in this case, the installer creates a log file in %temp% with the random name: MSI\*.LOG.</span></span> <span data-ttu-id="2ffff-106">Specificare la modalità di registrazione impostando il valore dei criteri su una stringa di caratteri.</span><span class="sxs-lookup"><span data-stu-id="2ffff-106">Specify the logging mode by setting the policy value to a string of characters.</span></span> <span data-ttu-id="2ffff-107">Utilizzare gli stessi caratteri per specificare i criteri della modalità di registrazione utilizzati dall'opzione della [riga di comando](command-line-options.md)"/l".</span><span class="sxs-lookup"><span data-stu-id="2ffff-107">Use the same characters to specify logging mode policy as used by the "/L" [command line option](command-line-options.md).</span></span> <span data-ttu-id="2ffff-108">Si noti che non è possibile usare "+" e " \* " per i criteri.</span><span class="sxs-lookup"><span data-stu-id="2ffff-108">Note that you cannot use "+" and "\*" for the policy.</span></span>

<span data-ttu-id="2ffff-109">La modalità di registrazione può essere impostata tramite i criteri, un'opzione della riga di comando o a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="2ffff-109">The logging mode can be set using policy, a command line option, or programmatically.</span></span> <span data-ttu-id="2ffff-110">Per ulteriori informazioni su tutti i metodi disponibili per l'impostazione della modalità di registrazione, vedere [registrazione normale](normal-logging.md) nella sezione [registrazione Windows Installer](windows-installer-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="2ffff-110">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="2ffff-111">È possibile impedire che le informazioni riservate, ad esempio le password, vengano immesse nel file di log e rese visibili.</span><span class="sxs-lookup"><span data-stu-id="2ffff-111">You can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span> <span data-ttu-id="2ffff-112">Per ulteriori informazioni, vedere la pagina relativa alla [prevenzione della scrittura di informazioni riservate nel file di log](preventing-confidential-information-from-being-written-into-the-log-file.md)</span><span class="sxs-lookup"><span data-stu-id="2ffff-112">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="registry-key"></a><span data-ttu-id="2ffff-113">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="2ffff-113">Registry Key</span></span>

<span data-ttu-id="2ffff-114">Impostare il valore denominato Logging sotto la chiave del registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="2ffff-114">Set the value named Logging under the following registry key.</span></span>

<span data-ttu-id="2ffff-115">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="2ffff-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="2ffff-116">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2ffff-116">Data Type</span></span>

<span data-ttu-id="2ffff-117">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="2ffff-117">**REG\_SZ**</span></span>

 

 



