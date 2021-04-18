---
description: Prima che un'applicazione possa aggiungere dati al registro di sistema, deve creare o aprire una chiave.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Apertura, creazione e chiusura di chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3260c255240ce2c7fb5d13fe28126a1a3f5527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308097"
---
# <a name="opening-creating-and-closing-keys"></a><span data-ttu-id="469de-103">Apertura, creazione e chiusura di chiavi</span><span class="sxs-lookup"><span data-stu-id="469de-103">Opening, Creating, and Closing Keys</span></span>

<span data-ttu-id="469de-104">Prima che un'applicazione possa aggiungere dati al registro di sistema, deve creare o aprire una chiave.</span><span class="sxs-lookup"><span data-stu-id="469de-104">Before an application can add data to the registry, it must create or open a key.</span></span> <span data-ttu-id="469de-105">Per creare o aprire una chiave, un'applicazione fa sempre riferimento alla chiave come sottochiave di una chiave attualmente aperta.</span><span class="sxs-lookup"><span data-stu-id="469de-105">To create or open a key, an application always refers to the key as a subkey of a currently open key.</span></span> <span data-ttu-id="469de-106">Le seguenti chiavi predefinite sono sempre aperte: **HKEY \_ Local \_ computer**, **HKEY \_ Classes \_ root**, **HKEY \_ Users** e **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="469de-106">The following predefined keys are always open: **HKEY\_LOCAL\_MACHINE**, **HKEY\_CLASSES\_ROOT**, **HKEY\_USERS**, and **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="469de-107">Un'applicazione usa la funzione [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) per aprire una chiave e la funzione [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) per creare una chiave.</span><span class="sxs-lookup"><span data-stu-id="469de-107">An application uses the [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) function to open a key and the [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) function to create a key.</span></span> <span data-ttu-id="469de-108">Un albero del registro di sistema può avere una profondità di 512 livelli.</span><span class="sxs-lookup"><span data-stu-id="469de-108">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="469de-109">È possibile creare fino a 32 livelli alla volta tramite una singola chiamata API del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="469de-109">You can create up to 32 levels at a time through a single registry API call.</span></span>

<span data-ttu-id="469de-110">Un'applicazione può usare la funzione [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) per chiudere una chiave e scrivere i dati in esso contenuti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="469de-110">An application can use the [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) function to close a key and write the data it contains into the registry.</span></span> <span data-ttu-id="469de-111">**RegCloseKey** non scrive necessariamente i dati nel registro di sistema prima di restituire; il scaricamento della cache sul disco rigido può richiedere fino a pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="469de-111">**RegCloseKey** does not necessarily write the data to the registry before returning; it can take as much as several seconds for the cache to be flushed to the hard disk.</span></span> <span data-ttu-id="469de-112">Se un'applicazione deve scrivere in modo esplicito i dati del registro di sistema sul disco rigido, può usare la funzione [**RegFlushKey ha**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) .</span><span class="sxs-lookup"><span data-stu-id="469de-112">If an application must explicitly write registry data to the hard disk, it can use the [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) function.</span></span> <span data-ttu-id="469de-113">**RegFlushKey ha**, tuttavia, utilizza molte risorse di sistema e deve essere chiamato solo quando è strettamente necessario.</span><span class="sxs-lookup"><span data-stu-id="469de-113">**RegFlushKey**, however, uses many system resources and should be called only when absolutely necessary.</span></span>

 

 



