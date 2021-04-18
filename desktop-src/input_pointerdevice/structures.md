---
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le strutture dello stack di input del dispositivo puntatore.
ms.assetid: 33DCB172-8D95-4205-AE2E-ADD7F3BF988A
title: Strutture (input del dispositivo puntatore)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 988a66a65581cf97406ace5481f115b15a29329a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334029"
---
# <a name="pointer-device-input-stack-structures"></a><span data-ttu-id="2e2a0-103">Strutture dello stack di input del dispositivo puntatore</span><span class="sxs-lookup"><span data-stu-id="2e2a0-103">Pointer Device Input Stack structures</span></span>

<span data-ttu-id="2e2a0-104">Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le strutture [dello stack di input del dispositivo puntatore](pointer-device-stack-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="2e2a0-104">The topics in this section provide the reference specifications for [Pointer Device Input Stack](pointer-device-stack-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2e2a0-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="2e2a0-105">In this section</span></span>

| <span data-ttu-id="2e2a0-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="2e2a0-106">Topic</span></span> | <span data-ttu-id="2e2a0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e2a0-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="2e2a0-108">**POINTER_DEVICE_CURSOR_INFO**</span><span class="sxs-lookup"><span data-stu-id="2e2a0-108">**POINTER_DEVICE_CURSOR_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_cursor_info)<br/> | <span data-ttu-id="2e2a0-109">Contiene i mapping degli ID del cursore per i dispositivi puntatore.</span><span class="sxs-lookup"><span data-stu-id="2e2a0-109">Contains cursor ID mappings for pointer devices.</span></span><br/> |
| [<span data-ttu-id="2e2a0-110">**POINTER_DEVICE_INFO**</span><span class="sxs-lookup"><span data-stu-id="2e2a0-110">**POINTER_DEVICE_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_info)<br/> | <span data-ttu-id="2e2a0-111">Contiene informazioni su un dispositivo puntatore.</span><span class="sxs-lookup"><span data-stu-id="2e2a0-111">Contains information about a pointer device.</span></span> <span data-ttu-id="2e2a0-112">Una matrice di queste strutture viene restituita dalla funzione [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) .</span><span class="sxs-lookup"><span data-stu-id="2e2a0-112">An array of these structures is returned from the [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) function.</span></span> <span data-ttu-id="2e2a0-113">Una singola struttura viene restituita da una chiamata alla funzione [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) .</span><span class="sxs-lookup"><span data-stu-id="2e2a0-113">A single structure is returned from a call to the [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) function.</span></span> <br/> |
| [<span data-ttu-id="2e2a0-114">**POINTER_DEVICE_PROPERTY**</span><span class="sxs-lookup"><span data-stu-id="2e2a0-114">**POINTER_DEVICE_PROPERTY**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_property)<br/> | <span data-ttu-id="2e2a0-115">Contiene le proprietà del dispositivo (elementi globali HID (Human Interface Device) che corrispondono agli utilizzi HID).</span><span class="sxs-lookup"><span data-stu-id="2e2a0-115">Contains device properties (Human Interface Device (HID) global items that correspond to HID usages).</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="2e2a0-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2e2a0-116">Related topics</span></span>

[<span data-ttu-id="2e2a0-117">Riferimento allo stack di input del dispositivo puntatore</span><span class="sxs-lookup"><span data-stu-id="2e2a0-117">Pointer Device Input Stack Reference</span></span>](unified-input-stack-reference.md)
