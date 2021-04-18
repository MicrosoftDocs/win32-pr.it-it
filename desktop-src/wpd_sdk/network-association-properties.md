---
description: I dispositivi portatili Windows supportano le seguenti proprietà di associazione di rete.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Proprietà associazione di rete (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41e40e456d4671d1aa8fb190274afd2f5ace98b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328569"
---
# <a name="network-association-properties"></a><span data-ttu-id="4d1d0-103">Proprietà dell'associazione di rete</span><span class="sxs-lookup"><span data-stu-id="4d1d0-103">Network Association Properties</span></span>

<span data-ttu-id="4d1d0-104">I dispositivi portatili Windows supportano le seguenti proprietà di associazione di rete.</span><span class="sxs-lookup"><span data-stu-id="4d1d0-104">Windows Portable Devices supports the following network association properties.</span></span>



| <span data-ttu-id="4d1d0-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4d1d0-105">Property</span></span>                                                  | <span data-ttu-id="4d1d0-106">VarType</span><span class="sxs-lookup"><span data-stu-id="4d1d0-106">VarType</span></span>                   | <span data-ttu-id="4d1d0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d1d0-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d1d0-108">**\_ \_ \_ \_ identificatori di rete dell'host di associazione di rete WPD \_**</span><span class="sxs-lookup"><span data-stu-id="4d1d0-108">**WPD\_NETWORK\_ASSOCIATION\_HOST\_NETWORK\_IDENTIFIERS**</span></span> | <span data-ttu-id="4d1d0-109">**VT \_ vettore \| VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="4d1d0-109">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="4d1d0-110">Elenco di identificatori host EUI-64 validi per questa associazione. Si tratta di una matrice di byte che contiene un numero integrale di indirizzi di rete fisica EUI-64.</span><span class="sxs-lookup"><span data-stu-id="4d1d0-110">The list of EUI-64 host identifiers valid for this association.This is an array of bytes that contains an integral number of EUI-64 physical network addresses.</span></span> <span data-ttu-id="4d1d0-111">Questi valori EUI-64 sono gli indirizzi di rete fisici disponibili nell'host al momento dell'associazione di rete.</span><span class="sxs-lookup"><span data-stu-id="4d1d0-111">These EUI-64 values are the physical network addresses available on the host at Network Association time.</span></span> <span data-ttu-id="4d1d0-112">Se l'host dispone di indirizzi di rete fisica MAC-48 (tipici di reti IPv4), ogni indirizzo MAC-48 verrà codificato nell'indirizzo EUI-64 come due metà dell'indirizzo MAC-48 separato da FF-FF.</span><span class="sxs-lookup"><span data-stu-id="4d1d0-112">If the host has MAC-48 physical network addresses (typical of IPv4 networks), each MAC-48 address will be encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span><br/> |
| <span data-ttu-id="4d1d0-113">**\_ \_ X509V3SEQUENCE associazione di rete WPD \_**</span><span class="sxs-lookup"><span data-stu-id="4d1d0-113">**WPD\_NETWORK\_ASSOCIATION\_X509V3SEQUENCE**</span></span>             | <span data-ttu-id="4d1d0-114">**VT \_ vettore \| VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="4d1d0-114">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="4d1d0-115">Sequenza di certificati X. 509 v3 da fornire per l'autenticazione del server TLS.</span><span class="sxs-lookup"><span data-stu-id="4d1d0-115">The sequence of X.509 v3 certificates to be provided for TLS server authentication.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="4d1d0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d1d0-116">Requirements</span></span>



| <span data-ttu-id="4d1d0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d1d0-117">Requirement</span></span> | <span data-ttu-id="4d1d0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4d1d0-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d1d0-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d1d0-119">Header</span></span><br/> | <dl> <span data-ttu-id="4d1d0-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d1d0-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d1d0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d1d0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d1d0-122">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="4d1d0-122">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




