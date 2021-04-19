---
description: Se il criterio di sistema per computer è impostato su &\# 0034; 1&\# 0034;, il programma di installazione impedisce agli utenti non amministratori di usare l'applicazione di patch per il controllo dell'account utente (UAC) per qualsiasi applicazione installata nel computer.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319969"
---
# <a name="disableluapatching"></a><span data-ttu-id="c2f36-103">DisableLUAPatching</span><span class="sxs-lookup"><span data-stu-id="c2f36-103">DisableLUAPatching</span></span>

<span data-ttu-id="c2f36-104">Se il criterio di sistema per computer è impostato su "1", il programma di installazione impedisce agli utenti non amministratori di usare l'applicazione di patch per il [controllo dell'account utente (UAC)](user-account-control--uac--patching.md) per qualsiasi applicazione installata nel computer.</span><span class="sxs-lookup"><span data-stu-id="c2f36-104">If this per-machine system policy is set to "1", the installer prevents non-administrators from using [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for any application installed on the computer.</span></span> <span data-ttu-id="c2f36-105">Quando il criterio di sistema per computer non è impostato o è impostato su 0, gli utenti non amministratori possono applicare patch utente con privilegi minimi alle applicazioni abilitate per l'applicazione di patch a un account utente con privilegi minimi.</span><span class="sxs-lookup"><span data-stu-id="c2f36-105">When the per-machine system policy is not set or set to 0, non-administrators can apply least-privilege user patches to applications that are enabled for least-privilege user account patching.</span></span>

<span data-ttu-id="c2f36-106">Utilizzare la proprietà [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) per impedire l'applicazione di patch con privilegi minimi.</span><span class="sxs-lookup"><span data-stu-id="c2f36-106">Use the [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) property to prevent the least-privilege patching of an application.</span></span>

<span data-ttu-id="c2f36-107">Il criterio DisableLUAPatching è disponibile a partire dalla versione Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="c2f36-107">The DisableLUAPatching policy is available beginning with Windows Installer version 3.0.</span></span>

## <a name="registry-key"></a><span data-ttu-id="c2f36-108">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c2f36-108">Registry Key</span></span>

<span data-ttu-id="c2f36-109">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="c2f36-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="c2f36-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c2f36-110">Data Type</span></span>

<span data-ttu-id="c2f36-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c2f36-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2f36-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2f36-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2f36-113">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="c2f36-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



