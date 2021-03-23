---
title: Gestione degli errori e della rimozione dei dispositivi in DirectML
description: In questo argomento viene illustrato come eseguire il debug della rimozione del dispositivo DirectML e di altre condizioni di errore.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b4567558b8b75685db16796e921f3daf35b849a1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548828"
---
# <a name="handling-errors-and-device-removal-in-directml"></a><span data-ttu-id="e655c-103">Gestione degli errori e della rimozione dei dispositivi in DirectML</span><span class="sxs-lookup"><span data-stu-id="e655c-103">Handling errors and device-removal in DirectML</span></span>

## <a name="device-removal"></a><span data-ttu-id="e655c-104">Rimozione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e655c-104">Device-removal</span></span>

<span data-ttu-id="e655c-105">Se si verifica un errore irreversibile, il dispositivo DirectML può entrare nello stato "dispositivo-rimosso".</span><span class="sxs-lookup"><span data-stu-id="e655c-105">If an unrecoverable error occurs, the DirectML device may enter a "device-removed" state.</span></span> <span data-ttu-id="e655c-106">Gli errori irreversibili che provocano la rimozione del dispositivo includono un utilizzo non valido dell'API (per i metodi che non restituiscono un valore [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), errori del driver, errori hardware o condizioni di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="e655c-106">Unrecoverable errors that cause device-removal include invalid API usage (for methods that don't return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), driver error, hardware fault, or out-of-memory (OOM) conditions.</span></span>

<span data-ttu-id="e655c-107">Quando un dispositivo DirectML viene rimosso, tutte le chiamate al metodo nel dispositivo e ogni oggetto creato da tale dispositivo diventano no-Ops.</span><span class="sxs-lookup"><span data-stu-id="e655c-107">When a DirectML device is removed, all method calls on the device, and every object created by that device, become no-ops.</span></span> <span data-ttu-id="e655c-108">Per i metodi che restituiscono un valore [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), viene restituito un codice di errore [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) .</span><span class="sxs-lookup"><span data-stu-id="e655c-108">For methods that return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), a [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) error code is returned.</span></span> <span data-ttu-id="e655c-109">È possibile usare il [metodo **IDMLDevice:: GetDeviceRemovedReason**](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) per verificare se il dispositivo DirectML è stato rimosso e per recuperare un codice di errore più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="e655c-109">You can use the [**IDMLDevice::GetDeviceRemovedReason** method](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) to check whether the DirectML device has been removed, and to retrieve a more detailed error code.</span></span>

<span data-ttu-id="e655c-110">Non è possibile eseguire il ripristino dalla rimozione del dispositivo tranne rilasciando il dispositivo interessato e tutti i relativi elementi figlio, quindi ricreando il dispositivo DirectML da zero.</span><span class="sxs-lookup"><span data-stu-id="e655c-110">You can't recover from device-removal except by releasing the affected device and all its children, then re-creating the DirectML device from scratch.</span></span>

<span data-ttu-id="e655c-111">Il dispositivo-la rimozione del dispositivo Direct3D 12 sottostante causa anche la rimozione del dispositivo DirectML.</span><span class="sxs-lookup"><span data-stu-id="e655c-111">Device-removal of the underlying Direct3D 12 device also causes the DirectML device to be removed.</span></span> <span data-ttu-id="e655c-112">Non è tuttavia consentito il contrario.</span><span class="sxs-lookup"><span data-stu-id="e655c-112">However, the reverse is not true.</span></span> <span data-ttu-id="e655c-113">Il dispositivo DirectML-la rimozione potrebbe non necessariamente far rimuovere il dispositivo Direct3D 12 sottostante.</span><span class="sxs-lookup"><span data-stu-id="e655c-113">DirectML device-removal may not necessarily cause the underlying Direct3D 12 device to become removed.</span></span>

## <a name="debugging-directml-device-removal-and-other-errors"></a><span data-ttu-id="e655c-114">Debug del dispositivo DirectML-rimozione e altri errori</span><span class="sxs-lookup"><span data-stu-id="e655c-114">Debugging DirectML device-removal, and other errors</span></span>

<span data-ttu-id="e655c-115">La ragione più comune degli errori DirectML è l'utilizzo dell'API non valido.</span><span class="sxs-lookup"><span data-stu-id="e655c-115">The most common cause of DirectML errors is invalid API usage.</span></span> <span data-ttu-id="e655c-116">Un utilizzo non valido dell'API potrebbe comportare un codice di errore HRESULT **E_INVALIDARG** o potrebbe causare la rimozione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e655c-116">Invalid API usage might result in an **E_INVALIDARG** HRESULT error code, or it might result in device-removal.</span></span>

<span data-ttu-id="e655c-117">Si consiglia di abilitare il livello di [debug DirectML](dml-debug-layer.md) durante lo sviluppo, per intercettare ed eseguire il debug di tali errori.</span><span class="sxs-lookup"><span data-stu-id="e655c-117">We strongly recommend that you enable the [DirectML debug layer](dml-debug-layer.md) during your development, in order to catch and debug such errors.</span></span> <span data-ttu-id="e655c-118">Il livello di debug DirectML esegue una convalida completa dei parametri del metodo e dell'utilizzo delle API e genera messaggi di output di debug che consentono di eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="e655c-118">The DirectML debug layer performs extensive validation of method parameters and API usage, and it will emit debug output messages to help you debug.</span></span>

## <a name="see-also"></a><span data-ttu-id="e655c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e655c-119">See also</span></span>

* [<span data-ttu-id="e655c-120">Uso del livello di debug DirectML</span><span class="sxs-lookup"><span data-stu-id="e655c-120">Using the DirectML debug layer</span></span>](dml-debug-layer.md)
