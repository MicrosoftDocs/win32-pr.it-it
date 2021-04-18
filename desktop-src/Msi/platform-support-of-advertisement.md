---
description: Il Windows Installer supporta l'annuncio di applicazioni e funzionalità.
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: Supporto della piattaforma per gli annunci
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320848"
---
# <a name="platform-support-of-advertisement"></a><span data-ttu-id="848c0-103">Supporto della piattaforma per gli annunci</span><span class="sxs-lookup"><span data-stu-id="848c0-103">Platform Support of Advertisement</span></span>

<span data-ttu-id="848c0-104">Il Windows Installer supporta l'annuncio di applicazioni e funzionalità.</span><span class="sxs-lookup"><span data-stu-id="848c0-104">The Windows Installer supports advertisement of applications and features.</span></span>

<span data-ttu-id="848c0-105">Le funzionalità di annuncio seguenti sono disponibili in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="848c0-105">The following advertisement capabilities are available on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP, and Windows 2000.</span></span>

-   <span data-ttu-id="848c0-106">Collegamenti e relative icone.</span><span class="sxs-lookup"><span data-stu-id="848c0-106">Shortcuts and their icons.</span></span>

-   <span data-ttu-id="848c0-107">Le estensioni e le rispettive icone specificate nella [tabella ProgId](progid-table.md).</span><span class="sxs-lookup"><span data-stu-id="848c0-107">Extensions and their icons specified in the [ProgId Table](progid-table.md).</span></span>

-   <span data-ttu-id="848c0-108">Verbi della shell e del comando registrati sotto la chiave ProgId.</span><span class="sxs-lookup"><span data-stu-id="848c0-108">Shell and command Verbs registered underneath the ProgId key.</span></span>

-   <span data-ttu-id="848c0-109">Contesti CLSID e InProcHandler.</span><span class="sxs-lookup"><span data-stu-id="848c0-109">CLSID contexts and InProcHandler.</span></span>

-   <span data-ttu-id="848c0-110">L'installazione su richiesta tramite OLE è disponibile solo a livello di codice tramite [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++) e la funzione **CreateObject (Visual Basic)** o la **funzione GetObject (Visual Basic)**.</span><span class="sxs-lookup"><span data-stu-id="848c0-110">Install-On-Demand through OLE is only available programmatically through [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++), and **CreateObject Function (Visual Basic)** or **GetObject Function (Visual Basic)**.</span></span>

> [!Note]
> <span data-ttu-id="848c0-111">Le informazioni su AppId e TypeLib vengono scritte solo quando viene installato un componente annunciato.</span><span class="sxs-lookup"><span data-stu-id="848c0-111">AppId and Typelib information is only written when an advertised component is installed.</span></span>
> 
> <span data-ttu-id="848c0-112">Per supportare le estensioni di file, l'applicazione deve essere pubblicata per Active Directory da un amministratore che usa Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="848c0-112">To support file name extensions, the application must be published to Active Directory by an administrator using Group Policy.</span></span>

## <a name="remarks"></a><span data-ttu-id="848c0-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="848c0-113">Remarks</span></span>

<span data-ttu-id="848c0-114">Per l'installazione del prodotto potrebbe non essere necessario un riavvio, ma tutti i tasti di scelta rapida annunciati non funzioneranno finché il computer non verrà riavviato.</span><span class="sxs-lookup"><span data-stu-id="848c0-114">The installation of the product may not require a restart, but any advertised shortcuts do not work until the machine is restarted.</span></span> <span data-ttu-id="848c0-115">I collegamenti annunciati per le installazioni successive funzionano senza riavvio.</span><span class="sxs-lookup"><span data-stu-id="848c0-115">The advertised shortcuts of subsequent installations work without a restart.</span></span>

<span data-ttu-id="848c0-116">Per assicurarsi che i collegamenti annunciati funzionino correttamente, l'autore del pacchetto deve pianificare un riavvio forzato alla fine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="848c0-116">To ensure that advertised shortcuts work correctly, the package author should schedule a forced restart at the end of the installation.</span></span>

<span data-ttu-id="848c0-117">Per evitare riavvii superflui del sistema, pianificare l'esecuzione di un riavvio solo se non è installata alcuna versione del Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="848c0-117">To avoid unnecessary restarts of the system, schedule a restart to run only if no version of the Windows Installer is installed.</span></span>

<span data-ttu-id="848c0-118">Le istruzioni condizionali possono controllare la proprietà [**ShellAdvtSupport**](shelladvtsupport.md) e la proprietà [**Version9X**](version9x.md) .</span><span class="sxs-lookup"><span data-stu-id="848c0-118">Conditional statements can check the [**ShellAdvtSupport**](shelladvtsupport.md) property and [**Version9X**](version9x.md) property.</span></span> <span data-ttu-id="848c0-119">Per ulteriori informazioni sulla pianificazione di un riavvio forzato condizionale, vedere [riavvii del sistema](system-reboots.md) e [utilizzo delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md).</span><span class="sxs-lookup"><span data-stu-id="848c0-119">For more information about scheduling a conditional forced restarts, see [System Reboots](system-reboots.md) and [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

 

 
