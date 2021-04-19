---
description: Nell'esempio di codice seguente viene illustrato l'utilizzo dell'oggetto TAPI per esaminare le risorse di telefonia disponibili per un indirizzo in grado di gestire un set specificato di requisiti del tipo di supporto. In questo esempio, audio e video sono i supporti necessari.
ms.assetid: 8be40a87-931d-4cda-9ef7-f9c0489e0b7b
title: Selezionare un indirizzo
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: da41059c38328ff00271e4fa561561eecf83e1cb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323872"
---
# <a name="select-an-address"></a><span data-ttu-id="fac91-104">Selezionare un indirizzo</span><span class="sxs-lookup"><span data-stu-id="fac91-104">Select an Address</span></span>

<span data-ttu-id="fac91-105">Nell'esempio di codice seguente viene illustrato l'utilizzo dell'oggetto TAPI per esaminare le risorse di telefonia disponibili per un indirizzo in grado di gestire un set specificato di requisiti del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="fac91-105">The following code example demonstrates use of the TAPI object to examine available telephony resources for an address that can handle a specified set of media type requirements.</span></span> <span data-ttu-id="fac91-106">In questo esempio, audio e video sono i supporti necessari.</span><span class="sxs-lookup"><span data-stu-id="fac91-106">In this example, audio and video are the required media.</span></span>

<span data-ttu-id="fac91-107">Prima di usare questo esempio di codice, è necessario eseguire le operazioni in [Initialize TAPI](initialize-tapi.md).</span><span class="sxs-lookup"><span data-stu-id="fac91-107">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="fac91-108">Questo esempio non include il controllo degli errori e le versioni appropriate per il codice di produzione.</span><span class="sxs-lookup"><span data-stu-id="fac91-108">This example doesn't have the error checking and releases appropriate for production code.</span></span>

```cpp
// Declare the interfaces used to select an address.
IEnumAddress * pIEnumAddress;
ITAddress * pAddress;
ITMediaSupport * pMediaSupport;

// Use the TAPI object to enumerate available addresses.
hr = gpTapi->EnumerateAddresses( &pIEnumAddress );
// If (hr != S_OK) process the error here. 

// Locate an address that can support the media type the application needs.
while ( S_OK == pIEnumAddress->Next(1, &pAddress, NULL) )
{
    // Determine the media support.
    hr = pAddress->QueryInterface(
         IID_ITMediaSupport,
         (void **)&pMediaSupport
         );
    // If (hr != S_OK) process the error here. 

    // In this example, the required media type is already known.
    // The application can also use the address object to
    // enumerate the media supported, then choose from there.
    hr = pMediaSupport->QueryMediaType(
         TAPIMEDIATYPE_AUDIO|TAPIMEDIATYPE_VIDEO,
         &bSupport
         );
    // If (hr != S_OK) process the error here. 

    if (bSupport)
    {
        break;
    }
}
// pAddress is now a usable address.
```

## <a name="related-topics"></a><span data-ttu-id="fac91-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fac91-109">Related topics</span></span>

[<span data-ttu-id="fac91-110">ITTAPI::EnumerateAddresses</span><span class="sxs-lookup"><span data-stu-id="fac91-110">ITTAPI::EnumerateAddresses</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)

[<span data-ttu-id="fac91-111">ITMediaSupport</span><span class="sxs-lookup"><span data-stu-id="fac91-111">ITMediaSupport</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)

[<span data-ttu-id="fac91-112">\_Costanti TAPIMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="fac91-112">TAPIMEDIATYPE\_ Constants</span></span>](tapimediatype--constants.md)
