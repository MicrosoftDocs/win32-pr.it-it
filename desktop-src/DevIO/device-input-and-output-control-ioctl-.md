---
description: La funzione DeviceIoControl fornisce un'interfaccia IOCTL (device input and Output Control) attraverso la quale un'applicazione può comunicare direttamente con un driver di dispositivo.
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: Controllo di input e output del dispositivo (IOCTL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2bb2ee26c63c2aad02d8e8d167ff12383fc6b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878130"
---
# <a name="device-input-and-output-control-ioctl"></a><span data-ttu-id="b6786-103">Controllo di input e output del dispositivo (IOCTL)</span><span class="sxs-lookup"><span data-stu-id="b6786-103">Device Input and Output Control (IOCTL)</span></span>

<span data-ttu-id="b6786-104">La funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) fornisce un'interfaccia IOCTL (device input and Output Control) attraverso la quale un'applicazione può comunicare direttamente con un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6786-104">The [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function provides a device input and output control (IOCTL) interface through which an application can communicate directly with a device driver.</span></span> <span data-ttu-id="b6786-105">La funzione **DeviceIoControl** è un'interfaccia generica che può inviare codici di controllo a un'ampia gamma di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b6786-105">The **DeviceIoControl** function is a general-purpose interface that can send control codes to a variety of devices.</span></span> <span data-ttu-id="b6786-106">Ogni codice di controllo rappresenta un'operazione che deve essere eseguita dal driver.</span><span class="sxs-lookup"><span data-stu-id="b6786-106">Each control code represents an operation for the driver to perform.</span></span> <span data-ttu-id="b6786-107">Ad esempio, un codice di controllo può chiedere a un driver di dispositivo di restituire informazioni sul dispositivo corrispondente o indirizzare il driver per eseguire un'azione sul dispositivo, ad esempio la formattazione di un disco.</span><span class="sxs-lookup"><span data-stu-id="b6786-107">For example, a control code can ask a device driver to return information about the corresponding device, or direct the driver to carry out an action on the device, such as formatting a disk.</span></span>

<span data-ttu-id="b6786-108">Nei file di intestazione dell'SDK sono definiti diversi codici di controllo standard.</span><span class="sxs-lookup"><span data-stu-id="b6786-108">A number of standard control codes are defined in the SDK header files.</span></span> <span data-ttu-id="b6786-109">Inoltre, i driver di dispositivo possono definire i propri codici di controllo specifici del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6786-109">In addition, device drivers can define their own device-specific control codes.</span></span> <span data-ttu-id="b6786-110">Per un elenco dei codici di controllo standard inclusi nella documentazione di SDK, vedere la sezione Osservazioni di [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span><span class="sxs-lookup"><span data-stu-id="b6786-110">For a list of standard control codes included in the SDK documentation, see the Remarks section of [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span></span>

<span data-ttu-id="b6786-111">I tipi di codici di controllo che è possibile specificare dipendono dal dispositivo a cui si accede e dalla piattaforma in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b6786-111">The types of control codes you can specify depend on the device being accessed and the platform on which your application is running.</span></span> <span data-ttu-id="b6786-112">Le applicazioni possono utilizzare i codici di controllo standard o i codici di controllo specifici del dispositivo per eseguire operazioni di input e output dirette su un'unità disco floppy, un'unità disco rigido, un'unità nastro o un'unità CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="b6786-112">Applications can use the standard control codes or device-specific control codes to perform direct input and output operations on a floppy disk drive, hard disk drive, tape drive, or CD-ROM drive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6786-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6786-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6786-114">Chiamata di DeviceIoControl</span><span class="sxs-lookup"><span data-stu-id="b6786-114">Calling DeviceIoControl</span></span>](calling-deviceiocontrol.md)
</dt> </dl>

 

 
