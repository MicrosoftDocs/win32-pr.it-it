---
description: 'Per Windows 7, i dispositivi portatili Windows supportano i seguenti attributi per i formati in un servizio del dispositivo. Questi attributi vengono restituiti dal metodo IPortableDeviceServiceCapabilities:: GetFormatAttributes.'
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Attributi di formato (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328963"
---
# <a name="format-attributes"></a><span data-ttu-id="805a3-104">Attributi di formato</span><span class="sxs-lookup"><span data-stu-id="805a3-104">Format Attributes</span></span>

<span data-ttu-id="805a3-105">Per Windows 7, i dispositivi portatili Windows supportano i seguenti attributi per i formati in un servizio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="805a3-105">For Windows 7, Windows Portable Devices supports the following attributes for formats on a device service.</span></span> <span data-ttu-id="805a3-106">Questi attributi vengono restituiti dal metodo [**IPortableDeviceServiceCapabilities:: GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) .</span><span class="sxs-lookup"><span data-stu-id="805a3-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method.</span></span>




| <span data-ttu-id="805a3-107">**Attributo**</span><span class="sxs-lookup"><span data-stu-id="805a3-107">**Attribute**</span></span>                        | <span data-ttu-id="805a3-108">**VarType**</span><span class="sxs-lookup"><span data-stu-id="805a3-108">**VarType**</span></span>    | <span data-ttu-id="805a3-109">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="805a3-109">**Description**</span></span>                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="805a3-110">**\_ \_ MIMETYPE attributo formato \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="805a3-110">**WPD\_FORMAT\_ATTRIBUTE\_MIMETYPE**</span></span> | <span data-ttu-id="805a3-111">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="805a3-111">**VT\_LPWSTR**</span></span> | <span data-ttu-id="805a3-112">Tipo MIME del formato.</span><span class="sxs-lookup"><span data-stu-id="805a3-112">The format MIME type.</span></span>                                                                                                     |
| <span data-ttu-id="805a3-113">**\_ \_ nome attributo formato \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="805a3-113">**WPD\_FORMAT\_ATTRIBUTE\_NAME**</span></span>     | <span data-ttu-id="805a3-114">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="805a3-114">**VT\_LPWSTR**</span></span> | <span data-ttu-id="805a3-115">Stringa che specifica il nome descrittivo per lo script del formato.</span><span class="sxs-lookup"><span data-stu-id="805a3-115">A string that specifies the script-friendly name of the format.</span></span> <span data-ttu-id="805a3-116">I caratteri validi sono alfanumerici \[ a-Za-z0-9 \] è \_ '.</span><span class="sxs-lookup"><span data-stu-id="805a3-116">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="805a3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="805a3-117">Requirements</span></span>



| <span data-ttu-id="805a3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="805a3-118">Requirement</span></span> | <span data-ttu-id="805a3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="805a3-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="805a3-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="805a3-120">Header</span></span><br/> | <dl> <span data-ttu-id="805a3-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="805a3-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805a3-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="805a3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805a3-123">**Proprietà e attributi**</span><span class="sxs-lookup"><span data-stu-id="805a3-123">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




