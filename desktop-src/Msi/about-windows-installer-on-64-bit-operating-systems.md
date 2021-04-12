---
description: Windows Installer viene eseguito come servizio nei computer che utilizzano Windows a 32 bit o a 64 bit.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: Informazioni Windows Installer sui sistemi operativi a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "104234369"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a><span data-ttu-id="ab8d5-103">Informazioni Windows Installer sui sistemi operativi a 64 bit</span><span class="sxs-lookup"><span data-stu-id="ab8d5-103">About Windows Installer on 64-Bit Operating Systems</span></span>

<span data-ttu-id="ab8d5-104">Windows Installer viene eseguito come servizio nei computer che utilizzano Windows a 32 bit o a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-104">Windows Installer runs as a service on computers using 32-bit or 64-bit Windows.</span></span> <span data-ttu-id="ab8d5-105">Le versioni del programma di installazione precedenti alla versione 2,0 possono installare e gestire i pacchetti Windows Installer a 32 bit solo nei sistemi operativi a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-105">Versions of the installer earlier than version 2.0 can install and manage 32-bit Windows Installer Packages only on 32-bit operating systems.</span></span> <span data-ttu-id="ab8d5-106">Si noti che non è possibile pubblicizzare o installare un'applicazione a 64 bit in un sistema operativo a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-106">Note that you cannot advertise or install a 64-bit application on a 32-bit operating system.</span></span>

<span data-ttu-id="ab8d5-107">È necessario specificare un pacchetto di Windows Installer come pacchetto a 32 bit o a 64 bit. non può essere specificato come neutro.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-107">A Windows Installer package must be specified as either a 32-bit or a 64-bit package; it cannot be specified as neutral.</span></span> <span data-ttu-id="ab8d5-108">In un computer che utilizza un sistema operativo a 64 bit, il servizio Windows Installer è ospitato in un processo a 64 bit che consente di installare sia i pacchetti 32 bit che quelli a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-108">On a computer using a 64-bit operating system, the Windows Installer service is hosted in a 64-bit process that installs both 32-bit and 64-bit packages.</span></span> <span data-ttu-id="ab8d5-109">Windows Installer installa tre tipi di pacchetti di Windows Installer in un computer in cui è in esecuzione un sistema operativo a 64 bit:</span><span class="sxs-lookup"><span data-stu-id="ab8d5-109">Windows Installer installs three types of Windows installer packages on a computer running a 64-bit operating system:</span></span>

-   <span data-ttu-id="ab8d5-110">Pacchetti a 32 bit che contengono solo componenti a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-110">32-bit packages that contain only 32-bit components.</span></span>
-   <span data-ttu-id="ab8d5-111">Pacchetti a 64 bit contenenti alcuni componenti a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-111">64-bit packages containing some 32-bit components.</span></span>
-   <span data-ttu-id="ab8d5-112">Pacchetti a 64 bit contenenti solo componenti a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-112">64-bit packages containing only 64-bit components.</span></span>

<span data-ttu-id="ab8d5-113">Le sezioni seguenti descrivono i due tipi di pacchetti di Windows Installer e le nuove proprietà del programma di installazione fornite da Windows Installer per i pacchetti a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-113">The follow sections describe the two types of Windows Installer packages and the new installer properties provided by Windows Installer for 64-bit packages.</span></span>

[<span data-ttu-id="ab8d5-114">Pacchetti Windows Installer a 32 bit</span><span class="sxs-lookup"><span data-stu-id="ab8d5-114">32-bit Windows Installer Packages</span></span>](32-bit-windows-installer-packages.md)

[<span data-ttu-id="ab8d5-115">Pacchetti Windows Installer a 64 bit</span><span class="sxs-lookup"><span data-stu-id="ab8d5-115">64-bit Windows Installer Packages</span></span>](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a><span data-ttu-id="ab8d5-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ab8d5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab8d5-117">Uso di pacchetti di Windows Installer a 64 bit</span><span class="sxs-lookup"><span data-stu-id="ab8d5-117">Using 64-Bit Windows Installer Packages</span></span>](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



