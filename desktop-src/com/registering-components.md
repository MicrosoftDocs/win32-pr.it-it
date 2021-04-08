---
title: Registrazione di componenti
description: Registrazione di componenti
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d683ae419466d62d764283cfa8706981de402a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047401"
---
# <a name="registering-components"></a><span data-ttu-id="75b6f-103">Registrazione di componenti</span><span class="sxs-lookup"><span data-stu-id="75b6f-103">Registering Components</span></span>

<span data-ttu-id="75b6f-104">Quando vengono installati i seguenti tipi di applicazioni, è necessario aggiungere le informazioni di installazione al registro di sistema, in genere tramite un programma di installazione:</span><span class="sxs-lookup"><span data-stu-id="75b6f-104">When the following types of applications are installed, installation information must be added to the registry, usually through a setup program:</span></span>

-   <span data-ttu-id="75b6f-105">Applicazioni server</span><span class="sxs-lookup"><span data-stu-id="75b6f-105">Server applications</span></span>
-   <span data-ttu-id="75b6f-106">Applicazioni contenitore/server</span><span class="sxs-lookup"><span data-stu-id="75b6f-106">Container/server applications</span></span>
-   <span data-ttu-id="75b6f-107">Applicazioni contenitore che consentono il collegamento a oggetti incorporati</span><span class="sxs-lookup"><span data-stu-id="75b6f-107">Container applications that allow linking to embedded objects</span></span>

<span data-ttu-id="75b6f-108">Per tutte e tre le istanze, registrare le informazioni della libreria COM (DLL) e le informazioni specifiche dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="75b6f-108">For all three instances, register COM library (DLL) information and application-specific information.</span></span>

<span data-ttu-id="75b6f-109">La DLL registra le informazioni per tutti i relativi componenti esportando [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="75b6f-109">The DLL registers the information for all its components by exporting [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="75b6f-110">Per registrare e annullare la registrazione di un componente, utilizzare le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="75b6f-110">Use the following functions to register and unregister a component:</span></span>

-   [<span data-ttu-id="75b6f-111">**RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="75b6f-111">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)
-   [<span data-ttu-id="75b6f-112">**RegCreateKeyEx**</span><span class="sxs-lookup"><span data-stu-id="75b6f-112">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="75b6f-113">**RegSetValueEx**</span><span class="sxs-lookup"><span data-stu-id="75b6f-113">**RegSetValueEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regsetvalueexa)
-   [<span data-ttu-id="75b6f-114">**RegEnumKeyEx**</span><span class="sxs-lookup"><span data-stu-id="75b6f-114">**RegEnumKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regenumkeyexa)
-   [<span data-ttu-id="75b6f-115">**RegDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="75b6f-115">**RegDeleteKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)
-   [<span data-ttu-id="75b6f-116">**RegCloseKey**</span><span class="sxs-lookup"><span data-stu-id="75b6f-116">**RegCloseKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regclosekey)

## <a name="related-topics"></a><span data-ttu-id="75b6f-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75b6f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75b6f-118">Registrazione di applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="75b6f-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 