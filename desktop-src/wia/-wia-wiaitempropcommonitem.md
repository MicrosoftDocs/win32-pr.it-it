---
description: Le seguenti costanti della proprietà del dispositivo devono essere supportate da tutte le interfacce di interfaccia IWiaItem, IWiaItem2 e IWiaDrvItem, se non diversamente specificato nelle descrizioni.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Costanti di proprietà degli elementi WIA comuni (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d36a390256c6a9d183caa0f9231d2a92035d83da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307291"
---
# <a name="common-wia-item-property-constants"></a><span data-ttu-id="6d1ff-103">Costanti comuni della proprietà dell'elemento WIA</span><span class="sxs-lookup"><span data-stu-id="6d1ff-103">Common WIA Item Property Constants</span></span>

<span data-ttu-id="6d1ff-104">Le seguenti costanti della proprietà del dispositivo devono essere supportate da tutte le interfacce di [interfaccia](https://msdn.microsoft.com/library/ms793976.aspx) [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) e IWiaDrvItem, se non diversamente specificato nelle descrizioni.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-104">The following device property constants must be supported by all [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) and [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) interfaces unless otherwise noted in their descriptions.</span></span>

<span data-ttu-id="6d1ff-105">Il prefisso "WIA \_ IPA \_ " indica una proprietà Item per tutti i dispositivi e rappresenta la convenzione di denominazione usata in C/C++.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-105">The prefix "WIA\_IPA\_" indicates an item property for all devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="6d1ff-106">Per finalità di scripting queste costanti usano il prefisso "Picture" e fanno parte del tipo enumerato [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-106">For scripting purposes these constants use the prefix "Picture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="6d1ff-107">Il nome del membro corrispondente da tale enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="6d1ff-108">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="6d1ff-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="6d1ff-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <span data-ttu-id="6d1ff-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6d1ff-111">Questo flag controlla l'accesso all'elemento e indica se l'elemento è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-111">This flag controls access to the item as well as whether the item is deleted.</span></span><br/> <span data-ttu-id="6d1ff-112">Obbligatorio per tutti gli elementi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-112">Required for all WIA 2.0 items.</span></span><br/> <span data-ttu-id="6d1ff-113">Tipo: <strong>VT_I4</strong>; Lettura/scrittura o sola lettura, a seconda della possibilità di modificare i diritti di accesso dell'elemento; Valori validi: WIA_PROP_FLAG</span><span class="sxs-lookup"><span data-stu-id="6d1ff-113">Type: <strong>VT_I4</strong>; Read/Write or Read Only, depending on the item's ability to have its access rights changed; Valid values: WIA_PROP_FLAG</span></span><br/> <span data-ttu-id="6d1ff-114">La tabella seguente include i cinque flag validi con questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-114">The following table has the five flags that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6d1ff-115">Diritto di accesso</span><span class="sxs-lookup"><span data-stu-id="6d1ff-115">Access Right</span></span></th>
<th><span data-ttu-id="6d1ff-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d1ff-117">WIA_ITEM_READ</span><span class="sxs-lookup"><span data-stu-id="6d1ff-117">WIA_ITEM_READ</span></span></td>
<td><span data-ttu-id="6d1ff-118">L'elemento dispone di accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-118">Item has read-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-119">WIA_ITEM_WRITE</span><span class="sxs-lookup"><span data-stu-id="6d1ff-119">WIA_ITEM_WRITE</span></span></td>
<td><span data-ttu-id="6d1ff-120">L'elemento dispone di accesso di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-120">Item has write-only access.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-121">WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="6d1ff-121">WIA_ITEM_CAN_BE_DELETED</span></span></td>
<td><span data-ttu-id="6d1ff-122">L'elemento dispone di accesso di sola eliminazione.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-122">Item has delete-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-123">WIA_ITEM_RD</span><span class="sxs-lookup"><span data-stu-id="6d1ff-123">WIA_ITEM_RD</span></span></td>
<td><span data-ttu-id="6d1ff-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="6d1ff-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-125">WIA_ITEM_RWD</span><span class="sxs-lookup"><span data-stu-id="6d1ff-125">WIA_ITEM_RWD</span></span></td>
<td><span data-ttu-id="6d1ff-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="6d1ff-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <span data-ttu-id="6d1ff-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-128">Questa proprietà è riservata da per un utilizzo futuro e non è implementata in questo momento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-128">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="6d1ff-129">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-129">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <span data-ttu-id="6d1ff-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-131">Contiene il numero di bit per canale per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-131">Contains the number of bits per channel for the image.</span></span> <span data-ttu-id="6d1ff-132">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-132">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-133">Obbligatorio per tutti gli elementi immagine archiviati o abilitati per l'acquisizione WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-133">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="6d1ff-134">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-134">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <span data-ttu-id="6d1ff-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-136">Contiene la dimensione del buffer, in byte, utilizzata durante il trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-136">Contains the size of the buffer, in bytes, used during a data transfer.</span></span> <span data-ttu-id="6d1ff-137">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-137">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-138">Un'applicazione può leggere questa proprietà per determinare le dimensioni del buffer specificate dal driver per i trasferimenti di dati.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-138">An application can read this property to determine the driver-specified buffer size for data transfers.</span></span> <span data-ttu-id="6d1ff-139">Il servizio WIA legge anche questa proprietà per allocare memoria per minidriver durante il trasferimento dei dati</span><span class="sxs-lookup"><span data-stu-id="6d1ff-139">The WIA service also reads this property to allocate memory for the minidriver during the data transfer</span></span></p>
<p><span data-ttu-id="6d1ff-140">Facoltativo per tutti gli elementi WIA 2,0 abilitati per il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-140">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-141">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-141">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6d1ff-142">Il <strong>WIA_IPA_BUFFER_SIZE</strong> proprietà contiene è la quantità minima di dati che un'applicazione può richiedere in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-142">The <strong>WIA_IPA_BUFFER_SIZE</strong> property contains is the minimum amount of data an application can request at any given time.</span></span> <span data-ttu-id="6d1ff-143">Maggiore è la dimensione del buffer, più grande sarà il numero di richieste al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-143">The larger the buffer size, the larger the requests to the device will be.</span></span> <span data-ttu-id="6d1ff-144">In questo modo il dispositivo può sembrare lento e non risponde, può rallentare le prestazioni complessive del sistema e può utilizzare risorse eccessive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-144">This can make the device seem slow and unresponsive, can slow the overall system performance, and can consume excessive resources.</span></span> <span data-ttu-id="6d1ff-145">Le dimensioni del buffer troppo piccole possono rallentare le prestazioni del trasferimento dei dati richiedendo molte richieste più piccole.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-145">Buffer sizes that are too small can slow performance of the data transfer by requiring many smaller requests.</span></span> <span data-ttu-id="6d1ff-146">Scegliere una dimensione del buffer ragionevole considerando le dimensioni tipiche di una richiesta di dati al dispositivo e bilanciare il numero di richieste rispetto alle dimensioni di tali richieste.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-146">Choose a reasonable buffer size by considering the typical size of a data request to your device and balancing the number of requests against the size of those requests.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <span data-ttu-id="6d1ff-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-148">Contiene il numero di byte in una riga di analisi dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-148">Contains the number of bytes in one scan line of the image.</span></span> <span data-ttu-id="6d1ff-149">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-149">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-150">Facoltativo per tutti gli elementi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-150">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-151">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-151">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <span data-ttu-id="6d1ff-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-153">Contiene il numero di canali per pixel per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-153">Contains the number of channels per pixel for the image.</span></span> <span data-ttu-id="6d1ff-154">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-154">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-155">Obbligatorio per tutti gli elementi immagine archiviati o abilitati per l'acquisizione WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-155">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="6d1ff-156">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-156">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <span data-ttu-id="6d1ff-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-158">Questa proprietà è riservata da per un utilizzo futuro e non è implementata in questo momento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-158">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="6d1ff-159">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-159">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <span data-ttu-id="6d1ff-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-161">Contiene il tipo di compressione corrente utilizzato.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-161">Contains the current compression type used.</span></span> <span data-ttu-id="6d1ff-162">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-162">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-163">Un'applicazione legge questa proprietà per determinare il tipo di compressione dell'immagine o imposta questa proprietà per configurare l'impostazione di compressione.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-163">An application reads this property to determine the image compression type or sets this property to configure the compression setting.</span></span></p>
<p><span data-ttu-id="6d1ff-164">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-164">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="6d1ff-165">La tabella seguente contiene le costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-165">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="6d1ff-166">Il simbolo <strong>V</strong> indica che la costante è supportata solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-166">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="6d1ff-167">È disponibile solo tramite l'interfaccia <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-167">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6d1ff-168">Tipo di compressione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-168">Compression Type</span></span></th>
<th><span data-ttu-id="6d1ff-169">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d1ff-170">WIA_COMPRESSION_NONE</span><span class="sxs-lookup"><span data-stu-id="6d1ff-170">WIA_COMPRESSION_NONE</span></span></td>
<td><span data-ttu-id="6d1ff-171">Nessuna compressione.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-171">No compression.</span></span> <span data-ttu-id="6d1ff-172">Per ulteriori informazioni, vedere la <strong>Nota</strong> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-172">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-173">WIA_COMPRESSION_AUTO</span><span class="sxs-lookup"><span data-stu-id="6d1ff-173">WIA_COMPRESSION_AUTO</span></span></td>
<td><span data-ttu-id="6d1ff-174">Modalità di compressione automatica.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-174">Automatic compression mode.</span></span> <span data-ttu-id="6d1ff-175">Per ulteriori informazioni, vedere la <strong>Nota</strong> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-175">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-176">WIA_COMPRESSION_BI_RLE4</span><span class="sxs-lookup"><span data-stu-id="6d1ff-176">WIA_COMPRESSION_BI_RLE4</span></span></td>
<td><span data-ttu-id="6d1ff-177">Compressione RLE4</span><span class="sxs-lookup"><span data-stu-id="6d1ff-177">RLE4 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-178">WIA_COMPRESSION_BI_RLE8</span><span class="sxs-lookup"><span data-stu-id="6d1ff-178">WIA_COMPRESSION_BI_RLE8</span></span></td>
<td><span data-ttu-id="6d1ff-179">Compressione RLE8</span><span class="sxs-lookup"><span data-stu-id="6d1ff-179">RLE8 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-180">WIA_COMPRESSION_G3</span><span class="sxs-lookup"><span data-stu-id="6d1ff-180">WIA_COMPRESSION_G3</span></span></td>
<td><span data-ttu-id="6d1ff-181">Compressione gruppo 3</span><span class="sxs-lookup"><span data-stu-id="6d1ff-181">Group 3 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-182">WIA_COMPRESSION_G4</span><span class="sxs-lookup"><span data-stu-id="6d1ff-182">WIA_COMPRESSION_G4</span></span></td>
<td><span data-ttu-id="6d1ff-183">Compressione gruppo 4</span><span class="sxs-lookup"><span data-stu-id="6d1ff-183">Group 4 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-184">WIA_COMPRESSION_JPEG</span><span class="sxs-lookup"><span data-stu-id="6d1ff-184">WIA_COMPRESSION_JPEG</span></span></td>
<td><span data-ttu-id="6d1ff-185">Compressione JPEG.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-185">JPEG compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-186">WIA_COMPRESSION_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-186">WIA_COMPRESSION_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="6d1ff-187">Compressione JBIG.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-187">JBIG compression.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span></span></td>
<td><span data-ttu-id="6d1ff-189">Compressione JPEG 2000.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-189">JPEG 2000 compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-190">WIA_COMPRESSION_PNG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-190">WIA_COMPRESSION_PNG<strong>V</strong></span></span></td>
<td><span data-ttu-id="6d1ff-191">Compressione PNG.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-191">PNG compression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="6d1ff-192">Quando questa proprietà è WIA_COMPRESSION_NONE e WIA_IPA_FORMAT è WiaImgFmt_PDFA o WiaImgFmt_XPS; quindi WIA_COMPRESSION_NONE indica che la modalità di compressione non è definita e che lo scanner deve scegliere una modalità.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-192">When this property is WIA_COMPRESSION_NONE, and WIA_IPA_FORMAT is either WiaImgFmt_PDFA or WiaImgFmt_XPS; then WIA_COMPRESSION_NONE means that the compression mode is undefined and the scanner must decide on a mode.</span></span></p>
<p><span data-ttu-id="6d1ff-193">WIA_COMPRESSION_AUTO è un nuovo valore della proprietà definito per la proprietà WIA_IPA_COMPRESSION.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-193">WIA_COMPRESSION_AUTO is a new property value defined for the WIA_IPA_COMPRESSION property.</span></span> <span data-ttu-id="6d1ff-194">Questo valore è valido per tutte le origini dati di immagini programmabili, inclusi il piano e il feeder.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-194">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="6d1ff-195">Quando questo valore è supportato dal mini driver WIA, il client dell'applicazione WIA può impostare WIA_IPA_COMPRESSION per abilitare il rilevamento della modalità di compressione automatica nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-195">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_COMPRESSION in order to enable automatic compression mode detection at the device.</span></span> <span data-ttu-id="6d1ff-196">WIA_COMPRESSION_AUTO può funzionare con e senza il colore automatico completo supportato o abilitato (WIA_DATA_AUTO e WIA_DEPTH_AUTO).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-196">WIA_COMPRESSION_AUTO can work with and without full auto-color being supported or enabled (WIA_DATA_AUTO and WIA_DEPTH_AUTO).</span></span></p>
<p><span data-ttu-id="6d1ff-197">WIA_COMPRESSION_AUTO è particolarmente utile con i formati di file di trasferimento che supportano più tipi di dati e profondità di bit, ad esempio WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-197">WIA_COMPRESSION_AUTO is most useful with transfer file formats that support multiple data types and bit depths, such as WiaImgFmt_RAW.</span></span> <span data-ttu-id="6d1ff-198">Per ulteriori informazioni sui formati di file di trasferimento, vedere WIA_IPA_FORMAT in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-198">For more information about transfer file formats, see WIA_IPA_FORMAT in this table.</span></span></p>
<p><span data-ttu-id="6d1ff-199">È Opitonal per il mini-driver WIA a sostenere WIA_COMPRESSION_AUTO.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-199">It is opitonal for the WIA mini-driver to suport WIA_COMPRESSION_AUTO.</span></span> <span data-ttu-id="6d1ff-200">Quando è supportato, il mini driver WIA non deve mai impostarlo come valore predefinito per WIA_IPA_COMPRESSION; solo l'applicazione WIA può impostare questo valore.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-200">When it is supported, the WIA mini-driver must never set it as the default value for WIA_IPA_COMPRESSION; only the WIA application can set this value.</span></span></p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <span data-ttu-id="6d1ff-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-202">Contiene l'impostazione del tipo di dati corrente per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-202">Contains the current data type setting for the device.</span></span> <span data-ttu-id="6d1ff-203">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-203">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-204">Un'applicazione legge questa proprietà per determinare il tipo di dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-204">An application reads this property to determine the data type of the image.</span></span> <span data-ttu-id="6d1ff-205">Un'applicazione scrive questa proprietà per impostare il tipo di dati corrente dell'immagine da trasferire.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-205">An application writes this property to set the current data type of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="6d1ff-206">Questa proprietà è obbligatoria per tutti gli elementi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-206">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="6d1ff-207">Deve essere in lettura/scrittura per tutti gli elementi abilitati per l'acquisizione WIA 2,0 e in sola lettura per gli elementi di archiviazione WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-207">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="6d1ff-208">Tipo: <strong>VT_I4</strong>; Accesso per i sistemi operativi precedenti a Windows Vista: questa proprietà è di sola lettura per le fotocamere e di lettura/scrittura per gli scanner; Accesso per Windows Vista e versioni successive: questa proprietà è di sola lettura per WIA_CATEGORY_FOLDER e WIA_CATEGORY_FINISHED_FILE elementi e in lettura/scrittura per tutte le altre categorie di elementi WIA 2,0; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-208">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: This property is Read Only for cameras and Read/Write for scanners; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="6d1ff-209">La tabella seguente contiene le sei costanti valide con quando <strong>WIA_IPA_FORMAT</strong> non è impostato su WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-209">The following table has the six constants that are valid with when <strong>WIA_IPA_FORMAT</strong> is not set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6d1ff-210">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6d1ff-210">Data Type</span></span></th>
<th><span data-ttu-id="6d1ff-211">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-211">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d1ff-212">WIA_DATA_AUTO</span><span class="sxs-lookup"><span data-stu-id="6d1ff-212">WIA_DATA_AUTO</span></span></td>
<td><span data-ttu-id="6d1ff-213">Valido per tutte le origini dati di immagini programmabili, inclusi il piano e il feeder.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-213">Valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="6d1ff-214">Quando questo valore è supportato dal mini driver WIA, il client dell'applicazione WIA può impostare WIA_IPA_DATATYPE per abilitare il rilevamento automatico dei colori sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-214">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DATATYPE in order to enable automatic color detection at the device.</span></span> <span data-ttu-id="6d1ff-215">Quando si imposta WIA_DATA_AUTO, il mini driver WIA deve aggiornare WIA_IPA_DEPTH sullo stesso elemento WIA_DEPTH_AUTO (che deve essere un valore supportato se il dispositivo supporta il colore automatico).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-215">When WIA_DATA_AUTO is set, the WIA mini-driver must update WIA_IPA_DEPTH on the same item to WIA_DEPTH_AUTO (which must be a supported value if the device supports automatic color).</span></span><br/> <span data-ttu-id="6d1ff-216">Si tratta di un valore facoltativo, ma è obbligatorio quando WIA_DEPTH_AUTO è supportato per WIA_IPA_DEPTH.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-216">This is an optional value, but it is required when WIA_DEPTH_AUTO is supported for WIA_IPA_DEPTH.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-217">WIA_DATA_COLOR</span><span class="sxs-lookup"><span data-stu-id="6d1ff-217">WIA_DATA_COLOR</span></span></td>
<td><span data-ttu-id="6d1ff-218">I dati di analisi sono di colore rosso, verde, blu (RGB).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-218">Scan data is red, green, blue (RGB) color.</span></span> <span data-ttu-id="6d1ff-219">Il formato completo dei colori viene descritto usando le proprietà WIA seguenti: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-219">The full color format is described using the following WIA properties: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span></span><br/> <span data-ttu-id="6d1ff-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span></span><br/> <span data-ttu-id="6d1ff-221"><strong>WIA_IPA_PLANAR</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-221"><strong>WIA_IPA_PLANAR</strong></span></span><br/> <span data-ttu-id="6d1ff-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span></span><br/> <span data-ttu-id="6d1ff-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span></span><br/> <span data-ttu-id="6d1ff-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-225">WIA_DATA_COLOR_DITHER</span><span class="sxs-lookup"><span data-stu-id="6d1ff-225">WIA_DATA_COLOR_DITHER</span></span></td>
<td><span data-ttu-id="6d1ff-226">Uguale a WIA_DATA_COLOR ad eccezione del fatto che i dati vengono retinati utilizzando il modello di dithering attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-226">Same as WIA_DATA_COLOR except that the data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-227">WIA_DATA_COLOR_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="6d1ff-227">WIA_DATA_COLOR_THRESHOLD</span></span></td>
<td><span data-ttu-id="6d1ff-228">Uguale a WIA_DATA_COLOR ad eccezione del fatto che il valore soglia viene usato durante l'analisi dei dati.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-228">Same as WIA_DATA_COLOR except that the threshold value is used when scanning the data.</span></span> <span data-ttu-id="6d1ff-229">I valori dei colori sul valore <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> vengono convertiti in luminosità completa; i colori sotto questo valore vengono convertiti in nero.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-229">Color values over the <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> value are converted to full brightness; colors under this value are converted to black.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-230">WIA_DATA_DITHER</span><span class="sxs-lookup"><span data-stu-id="6d1ff-230">WIA_DATA_DITHER</span></span></td>
<td><span data-ttu-id="6d1ff-231">I dati di analisi vengono retinati utilizzando il modello di dithering attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-231">Scan data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-232">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="6d1ff-232">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="6d1ff-233">L'analisi dei dati rappresenta l'intensità.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-233">Scan data represents intensity.</span></span> <span data-ttu-id="6d1ff-234">La tavolozza è una scala grigia fissa e equidistante, con una profondità specificata da <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-234">The palette is a fixed, equally-spaced gray scale with a depth specified by <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-235">WIA_DATA_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="6d1ff-235">WIA_DATA_THRESHOLD</span></span></td>
<td><span data-ttu-id="6d1ff-236">La soglia è un bit per pixel di dati in bianco e nero.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-236">The threshold is one bit per pixel of black-and-white data.</span></span> <span data-ttu-id="6d1ff-237">I dati sul valore corrente di <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> vengono convertiti in bianco; i dati sotto questo valore vengono convertiti in nero.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-237">Data over the current value of <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> is converted to white; data under this value is converted to black.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="6d1ff-238">La proprietà <strong>WIA_IPA_DATATYPE</strong> viene inoltre utilizzata per descrivere il tipo di trasferimento dati non elaborati da utilizzare quando l'applicazione imposta WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-238">The <strong>WIA_IPA_DATATYPE</strong> property is also used to describe the type of RAW data transfer to be used when the application sets WiaImgFmt_RAW.</span></span> <span data-ttu-id="6d1ff-239">Il driver deve impostare la proprietà <strong>WIA_IPA_DATATYPE</strong> su un elenco di valori consentiti da cui l'applicazione può selezionarne una.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-239">The driver should set the <strong>WIA_IPA_DATATYPE</strong> property to a list of allowed values from which the application can pick one.</span></span></p>
<p><span data-ttu-id="6d1ff-240">Se il dispositivo può essere impostato su un solo valore, creare un tipo di <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e inserire il valore valido al suo interno.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-240">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="6d1ff-241">Controllare la proprietà <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> per determinare la profondità del bit.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-241">Check the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property to determine the bit depth.</span></span> <span data-ttu-id="6d1ff-242">Questa proprietà in genere contiene un solo valore per le fotocamere.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-242">This property usually contains a single value for cameras.</span></span></p>
<p><span data-ttu-id="6d1ff-243">Nella tabella seguente sono elencate le costanti valide con <strong>WIA_IPA_DATATYPE</strong> quando <strong>WIA_IPA_FORMAT</strong> è impostato su WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-243">The following table lists the constants that are valid with <strong>WIA_IPA_DATATYPE</strong> when <strong>WIA_IPA_FORMAT</strong> is set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6d1ff-244">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6d1ff-244">Data Type</span></span></th>
<th><span data-ttu-id="6d1ff-245">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-245">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d1ff-246">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="6d1ff-246">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="6d1ff-247">L'analisi dei dati rappresenta l'intensità.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-247">Scan data represents intensity.</span></span> <span data-ttu-id="6d1ff-248">La tavolozza è una scala di grigi fissa e equidistante con una profondità specificata dalla proprietà <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-248">The palette is a fixed, equally spaced grayscale with a depth specified by the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span> <span data-ttu-id="6d1ff-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-250">WIA_DATA_RAW_BGR</span><span class="sxs-lookup"><span data-stu-id="6d1ff-250">WIA_DATA_RAW_BGR</span></span></td>
<td><span data-ttu-id="6d1ff-251">I dati di analisi si trova nello spazio dei nomi BGR (blu-verde-rosso).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-251">Scan data is in the BGR (blue-green-red) colorspace.</span></span> <span data-ttu-id="6d1ff-252">Il formato completo dei colori viene descritto con followingWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-252">The full color format is described using the followingWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span></span><br/> <span data-ttu-id="6d1ff-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span></span><br/> <span data-ttu-id="6d1ff-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span></span><br/> <span data-ttu-id="6d1ff-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span></span><br/> <span data-ttu-id="6d1ff-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span></span><br/> <span data-ttu-id="6d1ff-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-258">WIA_DATA_RAW_CMY</span><span class="sxs-lookup"><span data-stu-id="6d1ff-258">WIA_DATA_RAW_CMY</span></span></td>
<td><span data-ttu-id="6d1ff-259">I dati di analisi sono nello spazio dei colori cyan-magenta-yellow (CMY).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-259">Scan data is in the cyan-magenta-yellow (CMY) colorspace.</span></span> <span data-ttu-id="6d1ff-260">Il formato completo dei colori viene descritto utilizzando le stesse proprietà WIA del WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-260">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="6d1ff-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-262">WIA_DATA_RAW_CMYK</span><span class="sxs-lookup"><span data-stu-id="6d1ff-262">WIA_DATA_RAW_CMYK</span></span></td>
<td><span data-ttu-id="6d1ff-263">I dati di analisi sono nello spazio dei colori cyan-magenta-yellow-black (CMYK).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-263">Scan data is in the cyan-magenta-yellow-black (CMYK) colorspace.</span></span> <span data-ttu-id="6d1ff-264">Il formato completo dei colori viene descritto utilizzando le stesse proprietà WIA del WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-264">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="6d1ff-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 4.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-266">WIA_DATA_RAW_RGB</span><span class="sxs-lookup"><span data-stu-id="6d1ff-266">WIA_DATA_RAW_RGB</span></span></td>
<td><span data-ttu-id="6d1ff-267">I dati di analisi sono nello spazio dei nomi rosso-verde-blu (RGB).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-267">Scan data is in the red-green-blue (RGB) colorspace.</span></span> <span data-ttu-id="6d1ff-268">Il formato completo dei colori viene descritto utilizzando le stesse proprietà WIA del WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-268">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="6d1ff-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-270">WIA_DATA_RAW_YUV</span><span class="sxs-lookup"><span data-stu-id="6d1ff-270">WIA_DATA_RAW_YUV</span></span></td>
<td><span data-ttu-id="6d1ff-271">I dati di analisi si trova nello spazio dei nomi della differenza di luminosità blu (YUV).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-271">Scan data is in the luminance-blue difference-red difference (YUV) colorspace.</span></span> <span data-ttu-id="6d1ff-272">Il formato completo dei colori viene descritto utilizzando le stesse proprietà WIA del WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-272">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="6d1ff-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-274">WIA_DATA_RAW_YUVK</span><span class="sxs-lookup"><span data-stu-id="6d1ff-274">WIA_DATA_RAW_YUVK</span></span></td>
<td><span data-ttu-id="6d1ff-275">I dati di analisi si trova nello spazio dei nomi di luminanza Blue Difference-Red Difference-Black (YUVK).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-275">Scan data is in the luminance-blue difference-red difference-black (YUVK) colorspace.</span></span> <span data-ttu-id="6d1ff-276">Il formato completo dei colori viene descritto utilizzando le stesse proprietà WIA del WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-276">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="6d1ff-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 4.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <span data-ttu-id="6d1ff-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-279">WIA_IPA_DEPTH contiene l'impostazione della profondità di bit di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-279">WIA_IPA_DEPTH Contains the bit depth setting of an image.</span></span> <span data-ttu-id="6d1ff-280">Minidriver crea e gestisce questa proprietà. Un'applicazione legge questa proprietà per determinare l'impostazione della profondità di bit dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-280">The minidriver creates and maintains this property.An application reads this property to determine the bit depth setting of the image.</span></span> <span data-ttu-id="6d1ff-281">L'applicazione potrebbe anche essere in grado di impostare questo valore sulla profondità del bit desiderata.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-281">The application might also be able to set this value to the desired bit depth.</span></span></p>
<p><span data-ttu-id="6d1ff-282">Se il dispositivo può essere impostato su un solo valore, creare un tipo di <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e inserire il valore valido al suo interno.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-282">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="6d1ff-283">Questa proprietà è obbligatoria per tutti gli elementi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-283">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="6d1ff-284">Deve essere in lettura/scrittura per tutti gli elementi abilitati per l'acquisizione WIA 2,0 e in sola lettura per gli elementi di archiviazione WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-284">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="6d1ff-285">Tipo: <strong>VT_I4</strong>; Accesso per i sistemi operativi precedenti a Windows Vista: lettura/scrittura; Accesso per Windows Vista e versioni successive: questa proprietà è di sola lettura per WIA_CATEGORY_FOLDER e WIA_CATEGORY_FINISHED_FILE elementi e in lettura/scrittura per tutte le altre categorie di elementi WIA 2,0; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-285">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: Read/Write; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="6d1ff-286">WIA_DEPTH_AUTO è definito come 0 bit per pixel ed è un nuovo valore della proprietà definito per l'WIA_IPA_DEPTH.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-286">WIA_DEPTH_AUTO is defined as 0 bits per pixel, and it is a new property value defined for the WIA_IPA_DEPTH.</span></span> <span data-ttu-id="6d1ff-287">Questo valore è valido per tutte le origini dati di immagini programmabili, inclusi il piano e il feeder.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-287">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="6d1ff-288">Quando WIA_DEPTH_AUTO è supportato dal mini driver WIA, il client dell'applicazione WIA può impostare WIA_IPA_DEPTH su questo valore per abilitare il rilevamento automatico dei colori sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-288">When WIA_DEPTH_AUTO is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DEPTH to this value, to enable automatic color detection at the device.</span></span> <span data-ttu-id="6d1ff-289">Quando si imposta WIA_DEPTH_AUTO, il mini driver WIA deve aggiornare WIA_IPA_DATATYPE sullo stesso elemento WIA_DATA_AUTO (che deve essere un valore supportato, se il dispositivo supporta il colore automatico).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-289">When WIA_DEPTH_AUTO is set, the WIA mini-driver must update WIA_IPA_DATATYPE on the same item to WIA_DATA_AUTO (which must be a supported value, if the device supports automatic color).</span></span></p>
<p><span data-ttu-id="6d1ff-290">WIA_DEPTH_AUTO è un valore facoltativo, ma diventa necessario quando WIA_DATA_AUTO è supportato per WIA_IPA_DATATYPE.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-290">WIA_DEPTH_AUTO is an optional value, but it becomes required when WIA_DATA_AUTO is supported for WIA_IPA_DATATYPE.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <span data-ttu-id="6d1ff-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-292">Contiene l'estensione del nome file per un formato di file specifico.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-292">Contains the file name extension for a particular file format.</span></span> <span data-ttu-id="6d1ff-293">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-293">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-294">Facoltativo per tutti gli elementi WIA 2,0 abilitati per il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-294">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-295">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-295">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="6d1ff-296">Il driver Aggiorna questa proprietà per riflettere il valore corrente della proprietà <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-296">The driver updates this property to reflect the current value of the <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> property.</span></span></p>
<p><span data-ttu-id="6d1ff-297">Se, ad esempio, <strong>WIA_IPA_FORMAT</strong> è WiaImgFmt_JPEG, <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> dovrebbe essere <strong>jpg</strong>.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-297">For example, if <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_JPEG, then <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> should be <strong>jpg</strong>.</span></span> <span data-ttu-id="6d1ff-298">Se <strong>WIA_IPA_FORMAT</strong> è WiaImgFmt_BMP, WIA_IPA_FILENAME_EXTENSION dovrebbe essere BMP.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-298">If <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_BMP, then WIA_IPA_FILENAME_EXTENSION should be BMP.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6d1ff-299">L'estensione del nome file non include il punto.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-299">The file name extension does not include the dot.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6d1ff-300">Questa proprietà è consigliata per i driver che supportano formati standard ed è necessaria per i driver che implementano formati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-300">This property is recommended for drivers that support standard formats and is required for drivers that implement custom-defined formats.</span></span> <span data-ttu-id="6d1ff-301">Informa l'applicazione dell'estensione di file corretta da usare durante il trasferimento di file in formato privato.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-301">It informs the application of the correct file name extension to use during the transfer of privately formatted files.</span></span> <span data-ttu-id="6d1ff-302">Ad esempio, se A. Datum Corporation ha creato un driver WIA che ha trasferito un file in un nuovo formato, la società potrebbe specificare un'estensione di &quot; ADC &quot; .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-302">For example, if the A. Datum Corporation created a WIA driver that transferred a file in a new format, the company could specify an extension of &quot;adc&quot;.</span></span> <span data-ttu-id="6d1ff-303">In questo modo le applicazioni possono trasferire i dati in tale formato a un file e creare un nome file, ad esempio MyFile <em>. ADC</em>, che risulta utile per altri utenti che conoscono la nuova estensione.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-303">This allows applications to transfer data in that format to a file and to create a file name such as <em>myfile.adc</em>,which is useful to others who understand the new extension.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <span data-ttu-id="6d1ff-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-305">Contiene il formato corrente dell'immagine da trasferire.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-305">Contains the current format of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="6d1ff-306">Un'applicazione legge questa proprietà per determinare il formato dell'immagine che sta per ricevere.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-306">An application reads this property to determine the format of the image that it is about to receive.</span></span> <span data-ttu-id="6d1ff-307">Un'applicazione scrive questa proprietà per impostare il formato.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-307">An application writes this property to set the format.</span></span> <span data-ttu-id="6d1ff-308">Questa proprietà dipende dalla proprietà <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-308">This property depends on the <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> property.</span></span> <span data-ttu-id="6d1ff-309">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-309">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-310">Se il dispositivo può essere impostato su un solo valore, creare un tipo di <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e inserire il valore valido al suo interno.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-310">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="6d1ff-311">Tipo: <strong>CLSID</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-311">Type: <strong>CLSID</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="6d1ff-312">Nella tabella seguente sono elencate le costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-312">The following table lists the constants that are valid with this property.</span></span> <span data-ttu-id="6d1ff-313">L'asterisco \* indica che la costante non è supportata in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-313">The asterisk \* indicates that the constant is not supported in Windows Vista.</span></span> <span data-ttu-id="6d1ff-314">È disponibile solo tramite l'interfaccia <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> . Il doppio asterisco \* \* indica che la costante non è supportata in Windows Server 2003 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-314">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) The double asterisk \*\* indicates that the constant is not supported in either Windows Server 2003 or Windows Vista.</span></span> <span data-ttu-id="6d1ff-315">Il simbolo <strong>V</strong> indica che la costante è supportata solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-315">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="6d1ff-316">È disponibile solo tramite l'interfaccia <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-316">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6d1ff-317">Formato</span><span class="sxs-lookup"><span data-stu-id="6d1ff-317">Format</span></span></th>
<th><span data-ttu-id="6d1ff-318">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-318">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d1ff-319">WiaAudFmt_AIFF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-319">WiaAudFmt_AIFF</span></span></td>
<td><span data-ttu-id="6d1ff-320">Formato audio AIFF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-320">AIFF audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-321">WiaAudFmt_MP3</span><span class="sxs-lookup"><span data-stu-id="6d1ff-321">WiaAudFmt_MP3</span></span></td>
<td><span data-ttu-id="6d1ff-322">Formato audio MP3</span><span class="sxs-lookup"><span data-stu-id="6d1ff-322">MP3 audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-323">WiaAudFmt_WAV</span><span class="sxs-lookup"><span data-stu-id="6d1ff-323">WiaAudFmt_WAV</span></span></td>
<td><span data-ttu-id="6d1ff-324">Formato audio WAV</span><span class="sxs-lookup"><span data-stu-id="6d1ff-324">WAV audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-325">WiaAudFmt_WMA</span><span class="sxs-lookup"><span data-stu-id="6d1ff-325">WiaAudFmt_WMA</span></span></td>
<td><span data-ttu-id="6d1ff-326">Formato audio WMA</span><span class="sxs-lookup"><span data-stu-id="6d1ff-326">WMA audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-327">WiaImgFmt_ASF \* \*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-327">WiaImgFmt_ASF\*\*</span></span></td>
<td><span data-ttu-id="6d1ff-328">Formato video ASF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-328">ASF video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-329">WiaImgFmt_AVI \* \*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-329">WiaImgFmt_AVI\*\*</span></span></td>
<td><span data-ttu-id="6d1ff-330">Formato video AVI</span><span class="sxs-lookup"><span data-stu-id="6d1ff-330">AVI video format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-331">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="6d1ff-331">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="6d1ff-332">Bitmap di Windows con un file di intestazione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-332">Windows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-333">WiaImgFmt_CIFF \*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-333">WiaImgFmt_CIFF\*</span></span></td>
<td><span data-ttu-id="6d1ff-334">Formato del file di immagine della fotocamera</span><span class="sxs-lookup"><span data-stu-id="6d1ff-334">Camera Image File format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-335">WiaImgFmt_DPOF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-335">WiaImgFmt_DPOF</span></span></td>
<td><span data-ttu-id="6d1ff-336">Formato di stampa DPOF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-336">DPOF printing format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-337">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-337">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="6d1ff-338">Metafile Windows esteso</span><span class="sxs-lookup"><span data-stu-id="6d1ff-338">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-339">WiaImgFmt_EXEC</span><span class="sxs-lookup"><span data-stu-id="6d1ff-339">WiaImgFmt_EXEC</span></span></td>
<td><span data-ttu-id="6d1ff-340">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="6d1ff-340">Executable file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-341">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-341">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="6d1ff-342">Formato file scambiabile</span><span class="sxs-lookup"><span data-stu-id="6d1ff-342">Exchangeable File Format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-343">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="6d1ff-343">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="6d1ff-344">Formato FlashPix</span><span class="sxs-lookup"><span data-stu-id="6d1ff-344">FlashPix format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-345">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-345">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="6d1ff-346">Formato immagine GIF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-346">GIF image format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-347">WiaImgFmt_HTML</span><span class="sxs-lookup"><span data-stu-id="6d1ff-347">WiaImgFmt_HTML</span></span></td>
<td><span data-ttu-id="6d1ff-348">Formato HTML</span><span class="sxs-lookup"><span data-stu-id="6d1ff-348">HTML format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-349">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="6d1ff-349">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="6d1ff-350">Formato file icona Windows</span><span class="sxs-lookup"><span data-stu-id="6d1ff-350">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-351">WiaImgFmt_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-351">WiaImgFmt_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="6d1ff-352">Formato JBIG (Joint Image experts) di bi-level.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-352">The Joint Bi-level Image Experts Group (JBIG) format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-353">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="6d1ff-353">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="6d1ff-354">Formato compresso JPEG</span><span class="sxs-lookup"><span data-stu-id="6d1ff-354">JPEG compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-355">WiaImgFmt_JPEG2K</span><span class="sxs-lookup"><span data-stu-id="6d1ff-355">WiaImgFmt_JPEG2K</span></span></td>
<td><span data-ttu-id="6d1ff-356">Formato compresso JPEG 2000</span><span class="sxs-lookup"><span data-stu-id="6d1ff-356">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-357">WiaImgFmt_JPEG2KX</span><span class="sxs-lookup"><span data-stu-id="6d1ff-357">WiaImgFmt_JPEG2KX</span></span></td>
<td><span data-ttu-id="6d1ff-358">Formato compresso JPEG 2000</span><span class="sxs-lookup"><span data-stu-id="6d1ff-358">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-359">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="6d1ff-359">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="6d1ff-360">Bitmap di Windows senza un file di intestazione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-360">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-361">WiaImgFmt_PDFA<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-361">WiaImgFmt_PDFA<strong>V</strong></span></span></td>
<td><span data-ttu-id="6d1ff-362">Formato PDF/A (ISO/CD 19005-1).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-362">The PDF/A (ISO/CD 19005-1) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-363">WiaImgFmt_MPG \* \*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-363">WiaImgFmt_MPG\*\*</span></span></td>
<td><span data-ttu-id="6d1ff-364">Formato video MPEG</span><span class="sxs-lookup"><span data-stu-id="6d1ff-364">MPEG video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-365">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="6d1ff-365">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="6d1ff-366">Formato di file Eastman Kodak</span><span class="sxs-lookup"><span data-stu-id="6d1ff-366">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-367">WiaImgFmt_PICT</span><span class="sxs-lookup"><span data-stu-id="6d1ff-367">WiaImgFmt_PICT</span></span></td>
<td><span data-ttu-id="6d1ff-368">Formato di file Apple</span><span class="sxs-lookup"><span data-stu-id="6d1ff-368">Apple file format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-369">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="6d1ff-369">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="6d1ff-370">Formato PNG W3C</span><span class="sxs-lookup"><span data-stu-id="6d1ff-370">W3C PNG format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-371">WiaImgFmt_RAW</span><span class="sxs-lookup"><span data-stu-id="6d1ff-371">WiaImgFmt_RAW</span></span></td>
<td><span data-ttu-id="6d1ff-372">Formato non elaborato solo per i trasferimenti di dati</span><span class="sxs-lookup"><span data-stu-id="6d1ff-372">Raw format for data transfers only</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-373">WiaImgFmt_RAWRGB</span><span class="sxs-lookup"><span data-stu-id="6d1ff-373">WiaImgFmt_RAWRGB</span></span></td>
<td><span data-ttu-id="6d1ff-374">Formato RGB non elaborato</span><span class="sxs-lookup"><span data-stu-id="6d1ff-374">Raw RGB format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-375">WiaImgFmt_RTF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-375">WiaImgFmt_RTF</span></span></td>
<td><span data-ttu-id="6d1ff-376">Formato file RTF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-376">Rich Text File format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-377">WiaImgFmt_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="6d1ff-377">WiaImgFmt_SCRIPT</span></span></td>
<td><span data-ttu-id="6d1ff-378">File script</span><span class="sxs-lookup"><span data-stu-id="6d1ff-378">Script file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-379">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-379">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="6d1ff-380">Tag Image File Format</span><span class="sxs-lookup"><span data-stu-id="6d1ff-380">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-381">WiaImgFmt_TXT</span><span class="sxs-lookup"><span data-stu-id="6d1ff-381">WiaImgFmt_TXT</span></span></td>
<td><span data-ttu-id="6d1ff-382">File di testo</span><span class="sxs-lookup"><span data-stu-id="6d1ff-382">Text file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-383">WiaImgFmt_UNICODE16</span><span class="sxs-lookup"><span data-stu-id="6d1ff-383">WiaImgFmt_UNICODE16</span></span></td>
<td><span data-ttu-id="6d1ff-384">Codifica UNICODE a 16 bit</span><span class="sxs-lookup"><span data-stu-id="6d1ff-384">UNICODE 16-bit encoding</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-385">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-385">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="6d1ff-386">Metafile di Windows</span><span class="sxs-lookup"><span data-stu-id="6d1ff-386">Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-387">WiaImgFmt_XML</span><span class="sxs-lookup"><span data-stu-id="6d1ff-387">WiaImgFmt_XML</span></span></td>
<td><span data-ttu-id="6d1ff-388">File XML</span><span class="sxs-lookup"><span data-stu-id="6d1ff-388">XML file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-389">WiaImgFmt_XPS<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-389">WiaImgFmt_XPS<strong>V</strong></span></span></td>
<td><span data-ttu-id="6d1ff-390">Formato pacchetto XPS</span><span class="sxs-lookup"><span data-stu-id="6d1ff-390">XPS Package format</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6d1ff-391">Quando questa proprietà è WiaImgFmt_PDFA o WiaImgFmt_XPS e WIA_IPA_COMPRESSION è WIA_COMPRESSION_NONE; quindi, il secondo valore indica che la modalità di compressione non è definita e che lo scanner deve scegliere una modalità.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-391">When this property is either WiaImgFmt_PDFA or WiaImgFmt_XPS, and WIA_IPA_COMPRESSION is WIA_COMPRESSION_NONE; then the latter value means that the compression mode is undefined and the scanner must decide on a mode.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <span data-ttu-id="6d1ff-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-393">Contiene il nome dell'elemento completo (il nome dell'elemento insieme alle informazioni sul percorso).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-393">Contains the full item name (the item name together with path information).</span></span> <span data-ttu-id="6d1ff-394">Il nome dell'elemento completo corrisponde al parametro <em>bstrFullItemName</em> della funzione di utilità di servizio <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-394">The full item name is the same as the <em>bstrFullItemName</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="6d1ff-395">Un'applicazione legge questa proprietà per determinare l'elemento attualmente in uso e il punto in cui si trova nell'albero degli elementi.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-395">An application reads this property to determine which item it is currently using and where that item is located in the item tree.</span></span> <span data-ttu-id="6d1ff-396">Ogni elemento deve avere un nome univoco.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-396">Each item should have a unique name.</span></span> <span data-ttu-id="6d1ff-397">Le applicazioni usano comunemente il nome dell'elemento completo per cercare elementi nell'albero degli elementi.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-397">Applications commonly use the full item name to search for items in the item tree.</span></span> <span data-ttu-id="6d1ff-398">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-398">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-399">Obbligatorio per tutti gli elementi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-399">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-400">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-400">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <span data-ttu-id="6d1ff-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-402">Questa proprietà è riservata per un utilizzo futuro e non è implementata in questo momento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-402">This property is reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="6d1ff-403">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-403">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <span data-ttu-id="6d1ff-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-405">Contiene il nome del profilo ICM necessario per decodificare correttamente l'immagine.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-405">Contains the ICM profile name that is needed to properly decode the image.</span></span> <span data-ttu-id="6d1ff-406">Un'applicazione legge questa proprietà per determinare il profilo ICM da usare durante l'elaborazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-406">An application reads this property to determine the ICM profile to use when processing the image.</span></span> <span data-ttu-id="6d1ff-407">Il servizio WIA crea e gestisce questa proprietà in base alla voce ICMProfiles nel file di installazione del driver.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-407">The WIA service creates and maintains this property based on the ICMProfiles entry in the driver installation file.</span></span></p>
<p><span data-ttu-id="6d1ff-408">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-408">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <span data-ttu-id="6d1ff-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-410">Supportato solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-410">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="6d1ff-411">Gli elementi WIA 2,0 sono raggruppati in categorie che definiscono la modalità di trattamento o di utilizzo di un <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-411">WIA 2.0 items are grouped into categories that define how a <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> is to be treated or used.</span></span> <span data-ttu-id="6d1ff-412">Se, ad esempio, l'elemento rappresenta un feeder, l'applicazione deve prevedere che contenga le proprietà richieste del feed di documenti e funzioni come un feeder di documenti.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-412">For example, If the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="6d1ff-413">Se l'elemento rappresenta un file terminato, un'applicazione WIA 2,0 dovrebbe gestirla in questo modo, supponendo che i dati siano statici e presenti sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-413">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="6d1ff-414">(Le regole per ogni elemento verranno definite nei singoli documenti delle specifiche).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-414">(The rules for each item will be defined in their individual specification documents.)</span></span></p>
<p><span data-ttu-id="6d1ff-415">Obbligatorio per tutti gli elementi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-415">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-416">Tipo: <strong>VT_CLSID</strong>, accesso: sola lettura, valori validi: <a href="-wia-wia2-itemcategoryguids.md"><strong>GUID categoria elementi</strong></a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-416">Type: <strong>VT_CLSID</strong>, Access: Read Only, Valid values: <a href="-wia-wia2-itemcategoryguids.md"><strong>Item Category GUIDs</strong></a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <span data-ttu-id="6d1ff-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-418">Contiene i flag descrittivi per un elemento WIA.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-418">Contains the descriptive flags for a WIA item.</span></span> <span data-ttu-id="6d1ff-419">I flag dell'elemento corrispondono a quelli nel parametro <em>lObjectFlags</em> della funzione di utilità di servizio <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-419">The item flags are the same as those in the <em>lObjectFlags</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="6d1ff-420">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-420">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-421">Un'applicazione legge questa proprietà per determinare i valori del flag descrittivo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-421">An application reads this property to determine the item's descriptive flag values.</span></span></p>
<p><span data-ttu-id="6d1ff-422">Tipo: accesso <strong>VT_I4</strong> : sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-422">Type: <strong>VT_I4</strong> Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="6d1ff-423">La tabella seguente include i flag validi con questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-423">The following table has the flags that are valid with this property.</span></span> <span data-ttu-id="6d1ff-424">Un asterisco \* indica che il flag non è supportato in Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-424">An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="6d1ff-425">È disponibile solo tramite l'interfaccia <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> . Un asterisco doppio \* \* indica che il flag non è supportato in Windows Server 2003 o Windows Vista o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-425">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) An double asterisk \*\* indicates that the flag is not supported in either Windows Server 2003 or Windows Vista or later.</span></span> <span data-ttu-id="6d1ff-426">Il simbolo <strong>V</strong> indica che il flag è supportato solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-426">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> <span data-ttu-id="6d1ff-427">È disponibile solo tramite l'interfaccia <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-427">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6d1ff-428">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="6d1ff-428">Flag</span></span></th>
<th><span data-ttu-id="6d1ff-429">Definizione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-429">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d1ff-430">WiaItemTypeAnalyze\*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-430">WiaItemTypeAnalyze\*</span></span></td>
<td><span data-ttu-id="6d1ff-431">Questo elemento supporta il metodo <strong>IWiaItem:: AnalyzeItem</strong> (descritto nella documentazione di Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-431">This item supports the <strong>IWiaItem::AnalyzeItem</strong> method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="6d1ff-432">Questo elemento supporta anche la generazione automatica di elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-432">This item also supports automatic child item generation.</span></span> <span data-ttu-id="6d1ff-433">Questa funzionalità è utile per il rilevamento dell'area o la scomposizione della pagina.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-433">This capability is useful for region detection or page decomposition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-434">WiaItemTypeAudio</span><span class="sxs-lookup"><span data-stu-id="6d1ff-434">WiaItemTypeAudio</span></span></td>
<td><span data-ttu-id="6d1ff-435">Questo elemento supporta l'audio.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-435">This item supports audio.</span></span> <span data-ttu-id="6d1ff-436">Questo flag è valido solo per gli elementi in cui è impostato anche il flag <strong>WiaItemTypeFile</strong> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-436">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-437">WiaItemTypeBurst\*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-437">WiaItemTypeBurst\*</span></span></td>
<td><span data-ttu-id="6d1ff-438">Solo per le cartelle.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-438">For folders only.</span></span> <span data-ttu-id="6d1ff-439">Questo flag indica che le immagini in questa cartella sono state acquisite in una sequenza temporale continua.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-439">This flag indicates that the images in this folder were taken in a continuous time sequence.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-440">WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="6d1ff-440">WiaItemTypeDeleted</span></span></td>
<td><span data-ttu-id="6d1ff-441">Questo elemento è contrassegnato per l'eliminazione, questo elemento è stato eliminato, questo elemento non esiste o il contenuto di questo elemento non è valido.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-441">This item is marked for deletion, this item has been deleted, this item does not exist, or the contents of this item are invalid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-442">WiaItemTypeDocument<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-442">WiaItemTypeDocument<strong>V</strong></span></span></td>
<td><span data-ttu-id="6d1ff-443">Questo elemento è un file di documento in uno dei formati di documento contenuti nella proprietà <strong>WIA_IPA_FORMAT</strong> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-443">This item is a document file in one of the document formats that the <strong>WIA_IPA_FORMAT</strong> property contains.</span></span> <span data-ttu-id="6d1ff-444">Questi formati includono quelli per i file non di immagine, ad esempio i file con estensione txt, htm e doc.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-444">(These formats include those for nonimage files, such as .txt, .htm, and .doc files.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-445">WiaItemTypeDevice</span><span class="sxs-lookup"><span data-stu-id="6d1ff-445">WiaItemTypeDevice</span></span></td>
<td><span data-ttu-id="6d1ff-446">Questo elemento rappresenta un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-446">This item represents a connected device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-447">WiaItemTypeDisconnected</span><span class="sxs-lookup"><span data-stu-id="6d1ff-447">WiaItemTypeDisconnected</span></span></td>
<td><span data-ttu-id="6d1ff-448">Questo elemento rappresenta un dispositivo disconnesso.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-448">This item represents a disconnected device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-449">WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="6d1ff-449">WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="6d1ff-450">L'elemento supporta i trasferimenti di file.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-450">The item supports file transfers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-451">WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="6d1ff-451">WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="6d1ff-452">L'elemento è una cartella.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-452">The item is a folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-453">WiaItemTypeFree</span><span class="sxs-lookup"><span data-stu-id="6d1ff-453">WiaItemTypeFree</span></span></td>
<td><span data-ttu-id="6d1ff-454">L'elemento non è inizializzato o è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-454">The item is uninitialized or has been deleted.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-455">WiaItemTypeGenerated</span><span class="sxs-lookup"><span data-stu-id="6d1ff-455">WiaItemTypeGenerated</span></span></td>
<td><span data-ttu-id="6d1ff-456">Questo elemento è stato generato da un'applicazione o dal driver.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-456">This item has been generated by an application or by the driver.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-457">WiaItemTypeHasAttachments\*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-457">WiaItemTypeHasAttachments\*</span></span></td>
<td><span data-ttu-id="6d1ff-458">Questo elemento supporta gli allegati e attualmente contiene allegati.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-458">This item supports attachments and currently contains attachments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-459">WiaItemTypeHPanorama\*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-459">WiaItemTypeHPanorama\*</span></span></td>
<td><span data-ttu-id="6d1ff-460">Questo elemento rappresenta un'immagine panoramica orizzontale.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-460">This item represents a horizontal panoramic image.</span></span> <span data-ttu-id="6d1ff-461">Questo flag è valido solo per gli elementi in cui è impostato anche il flag <strong>WiaItemTypeFolder</strong> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-461">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-462">WiaItemTypeImage</span><span class="sxs-lookup"><span data-stu-id="6d1ff-462">WiaItemTypeImage</span></span></td>
<td><span data-ttu-id="6d1ff-463">L'elemento è un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-463">The item is an image file.</span></span> <span data-ttu-id="6d1ff-464">Questo flag è valido solo per gli elementi in cui è impostato anche il flag <strong>WiaItemTypeFile</strong> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-464">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-465">WiaItemTypeProgrammableDataSource<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-465">WiaItemTypeProgrammableDataSource<strong>V</strong></span></span></td>
<td><span data-ttu-id="6d1ff-466">L'elemento è un'origine dati programmabile e segue un set di regole di configurazione predefinite, basate su <strong>WIA_IPA_ITEM_CATEGORY</strong>.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-466">The item is a programmable data source and follows a set of predefined configuration rules, which are based on <strong>WIA_IPA_ITEM_CATEGORY</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-467">WiaItemTypeRoot<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ff-467">WiaItemTypeRoot<strong>V</strong></span></span></td>
<td><span data-ttu-id="6d1ff-468">Questo elemento è l'elemento radice, che è l'elemento padre di tutti gli elementi di funzionalità supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-468">This item is the root item, which is the parent to all the feature items that the device supports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-469">WiaItemTypeStorage</span><span class="sxs-lookup"><span data-stu-id="6d1ff-469">WiaItemTypeStorage</span></span></td>
<td><span data-ttu-id="6d1ff-470">Questo flag indica una risorsa di archiviazione aggiuntiva per gli elementi delle cartelle.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-470">This flag indicates additional storage for folders items.</span></span> <span data-ttu-id="6d1ff-471">I driver WIA specificano gli elementi in termini di immagini e cartelle.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-471">WIA drivers specify their items in terms of images and folders.</span></span> <span data-ttu-id="6d1ff-472">Non esistono proprietà WIA che descrivono le caratteristiche di un elemento di archiviazione (ad esempio, spazio di archiviazione rimanente, velocità di scrittura o tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-472">No WIA properties exist that describe the characteristics of a storage item (such as remaining storage space, write speed, or type of media.</span></span> <span data-ttu-id="6d1ff-473">È possibile aggiungere proprietà specifiche del fornitore che espongono queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-473">Vendor-specific properties that expose this information can be added.</span></span> <span data-ttu-id="6d1ff-474">Queste proprietà sono accessibili solo alle applicazioni o alle estensioni scritte per riconoscerle.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-474">These properties are accessible only to applications or extensions that are written to recognize them.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-475">WiaItemTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="6d1ff-475">WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="6d1ff-476">Questo elemento può essere usato per trasferire i dati.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-476">This item can be used to transfer data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-477">WiaItemTypeTwainCapabilityPassThrough</span><span class="sxs-lookup"><span data-stu-id="6d1ff-477">WiaItemTypeTwainCapabilityPassThrough</span></span></td>
<td><span data-ttu-id="6d1ff-478">Questo tipo indica che il dispositivo WIA è in grado di ricevere i dati sulle funzionalità TWAIN dal livello di compatibilità TWAIN.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-478">This type indicates that the WIA device is able to receive TWAIN capability data from the TWAIN compatibility layer.</span></span> <span data-ttu-id="6d1ff-479">Se questo tipo è impostato, qualsiasi funzionalità TWAIN non riconosciuta dal livello di compatibilità TWAIN verrà passata al driver theWIA.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-479">If this type is set, any TWAIN capability that is not understood by the TWAIN compatibility layer will be passed to theWIA driver.</span></span> <span data-ttu-id="6d1ff-480">Questo valore è valido solo per l'elemento radice.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-480">This is valid only for the root item.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-481">WiaItemTypeVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-481">WiaItemTypeVideo\*\*</span></span></td>
<td><span data-ttu-id="6d1ff-482">Questo elemento supporta lo streaming di video.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-482">This item supports streaming video.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-483">WiaItemTypeVPanorama\*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-483">WiaItemTypeVPanorama\*</span></span></td>
<td><span data-ttu-id="6d1ff-484">Questo elemento rappresenta un'immagine panoramica verticale.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-484">This item represents a vertical panoramic image.</span></span> <span data-ttu-id="6d1ff-485">Questo flag è valido solo per gli elementi in cui è impostato anche il flag <strong>WiaItemTypeFolder</strong> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-485">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="6d1ff-486">Alcuni di questi flag sono obbligatori o facoltativi per gli elementi WIA 2,0, in base alla categoria dell'elemento, come illustrato in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-486">Some of these flags are required or optional for WIA 2.0 items, according to the category of the item, as shown in this table.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6d1ff-487">Categoria dell'elemento</span><span class="sxs-lookup"><span data-stu-id="6d1ff-487">Category of Item</span></span></th>
<th><span data-ttu-id="6d1ff-488">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="6d1ff-488">Required</span></span></th>
<th><span data-ttu-id="6d1ff-489">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6d1ff-489">Optional</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d1ff-490">WIA_CATEGORY_ROOT</span><span class="sxs-lookup"><span data-stu-id="6d1ff-490">WIA_CATEGORY_ROOT</span></span></td>
<td><span data-ttu-id="6d1ff-491">WiaItemTypeRoot WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="6d1ff-491">WiaItemTypeRoot WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="6d1ff-492">WiaItemTypeDevice WiaItemTypeDisconnected</span><span class="sxs-lookup"><span data-stu-id="6d1ff-492">WiaItemTypeDevice WiaItemTypeDisconnected</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-493">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="6d1ff-493">WIA_CATEGORY_FLATBED</span></span></td>
<td><span data-ttu-id="6d1ff-494">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="6d1ff-494">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="6d1ff-495">WiaItemTypeFolder (se sono supportati più elementi delle aree di analisi, questo flag è facoltativo solo per l'elemento radice WIA_CATEGORY_FLATBED).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-495">WiaItemTypeFolder (If multiple scan regions items are supported, this flag is optional only for the WIA_CATEGORY_FLATBED root item.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span><span class="sxs-lookup"><span data-stu-id="6d1ff-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span></span></td>
<td><span data-ttu-id="6d1ff-497">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="6d1ff-497">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="6d1ff-498">WiaItemTypeFolder (se sono presenti WIA_CATEGORY_FEEDER_FRONT e WIA_CATEGORY_FEEDER_BACK elementi, questo flag è facoltativo solo per l'elemento radice WIA_CATEGORY_FEEDER).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-498">WiaItemTypeFolder (If WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK items are present, then this flag is optional only for the WIA_CATEGORY_FEEDER root item.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-499">WIA_CATEGORY_FILM (radice)</span><span class="sxs-lookup"><span data-stu-id="6d1ff-499">WIA_CATEGORY_FILM (root)</span></span></td>
<td><span data-ttu-id="6d1ff-500">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="6d1ff-500">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="6d1ff-501">nessuno</span><span class="sxs-lookup"><span data-stu-id="6d1ff-501">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-502">WIA_CATEGORY_FILM (elementi figlio)</span><span class="sxs-lookup"><span data-stu-id="6d1ff-502">WIA_CATEGORY_FILM (children)</span></span></td>
<td><span data-ttu-id="6d1ff-503">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="6d1ff-503">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="6d1ff-504">nessuno</span><span class="sxs-lookup"><span data-stu-id="6d1ff-504">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-505">WIA_CATEGORY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="6d1ff-505">WIA_CATEGORY_FOLDER</span></span></td>
<td><span data-ttu-id="6d1ff-506">WiaItemTypeStorage WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="6d1ff-506">WiaItemTypeStorage WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="6d1ff-507">WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="6d1ff-507">WiaItemTypeDeleted</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-508">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="6d1ff-508">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><span data-ttu-id="6d1ff-509">WiaItemTypeFile WiaItemTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="6d1ff-509">WiaItemTypeFile WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="6d1ff-510">WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="6d1ff-510">WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <span data-ttu-id="6d1ff-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-512">Contiene il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-512">Contains the item name.</span></span> <span data-ttu-id="6d1ff-513">Un'applicazione legge questa proprietà per determinare l'elemento attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-513">An application reads this property to determine which item it is currently using.</span></span> <span data-ttu-id="6d1ff-514">Ogni elemento ha un nome univoco.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-514">Each item has a unique name.</span></span> <span data-ttu-id="6d1ff-515">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-515">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-516">Obbligatorio per tutti gli elementi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-516">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-517">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-517">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <span data-ttu-id="6d1ff-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-519">Contiene le dimensioni correnti, in byte, dei dati associati all'elemento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-519">Contains the current size, in bytes, of the data that is associated with the item.</span></span> <span data-ttu-id="6d1ff-520">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-520">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-521">Contains è la dimensione totale dei dati da trasferire.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-521">Contains is the total size of the data being transferred.</span></span> <span data-ttu-id="6d1ff-522">Se questo valore è zero, significa che minidriver non dispone di informazioni sulle dimensioni esatte dei dati.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-522">If this value is zero, it means that the minidriver has no information about the exact size of the data.</span></span> <span data-ttu-id="6d1ff-523">(Si tratta di un problema comune per i dati compressi). Un'applicazione legge questo valore per determinare le dimensioni dell'acquisizione prima che avvenga.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-523">(This is common for compressed data.) An application reads this value to determine the size of the acquisition before it takes place.</span></span> <span data-ttu-id="6d1ff-524">Il servizio WIA legge questa proprietà per facilitare l'allocazione della memoria per i trasferimenti di dati.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-524">The WIA service reads this property to assist in allocating memory for data transfers.</span></span> <span data-ttu-id="6d1ff-525">Per ulteriori informazioni, vedere <a href="https://msdn.microsoft.com/library/ms792198.aspx">trasferimento di dati a un'applicazione WIA</a> se la proprietà è impostata su zero e tymed è configurato per un trasferimento di file, il servizio WIA non alloca alcuna memoria per il minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-525">For further information, see <a href="https://msdn.microsoft.com/library/ms792198.aspx">Transferring Data to a WIA Application</a> if the property is set to zero and TYMED is configured for a file transfer, the WIA service does not allocate any memory for the WIA minidriver.</span></span></p>
<p><span data-ttu-id="6d1ff-526">Obbligatorio per tutti gli elementi WIA 2,0 abilitati per il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-526">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-527">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-527">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <span data-ttu-id="6d1ff-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-529">Contiene l'ora in cui è stata originariamente acquisita l'immagine.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-529">Contains the time that the image was originally captured.</span></span> <span data-ttu-id="6d1ff-530">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-530">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="6d1ff-531">Questa proprietà deve essere segnalata come vettore di otto valori di <strong>parola</strong> sotto forma di una struttura SYSTEMTIME (descritta nella documentazione di Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="6d1ff-531">This property should be reported as a vector of eight <strong>WORD</strong> values in the form of a SYSTEMTIME structure (described in the Platform SDK documentation).</span></span></p>
<p><span data-ttu-id="6d1ff-532">Facoltativo per tutti gli elementi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-532">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-533">Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong> Access: lettura/scrittura o sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-533">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong> Access: Read/Write or Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="6d1ff-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-535">Supportato solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-535">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="6d1ff-536">Specifica il numero di elementi archiviati nell'elemento WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-536">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="6d1ff-537">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-537">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <span data-ttu-id="6d1ff-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-539">Specifica la dimensione minima del buffer utilizzata nei trasferimenti di dati.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-539">Specifies the minimum buffer size that is used in data transfers.</span></span> <span data-ttu-id="6d1ff-540">Se il trasferimento dei dati viene eseguito tramite un meccanismo di callback, il valore della proprietà può essere minimo di 64KB.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-540">If the data transfer is performed through a callback mechanism, the property value can be as small as 64KB.</span></span> <span data-ttu-id="6d1ff-541">Tuttavia, se il trasferimento è il file, il valore della proprietà è il numero di byte necessari per trasferire una pagina di dati alla volta.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-541">However, if the transfer is to file, the property value is the number of bytes that are needed to transfer one page of data at a time.</span></span> <span data-ttu-id="6d1ff-542">Minidriver crea e gestisce questa proprietà WIA.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-542">The minidriver creates and maintains this WIA property.</span></span></p>
<p><span data-ttu-id="6d1ff-543">Facoltativo per tutti gli elementi WIA 2,0 abilitati per il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-543">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-544">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-544">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <span data-ttu-id="6d1ff-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-546">Contiene il numero di righe contenute nell'immagine, ovvero l'altezza verticale dell'immagine in pixel.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-546">Contains the number of lines contained in the image (the vertical height of the image in pixels).</span></span> <span data-ttu-id="6d1ff-547">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-547">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-548">Facoltativo per tutti gli elementi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-548">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-549">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-549">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <span data-ttu-id="6d1ff-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-551">Contiene il numero di pixel in ogni riga dell'immagine, ovvero la larghezza dell'immagine in pixel.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-551">Contains the number of pixels in each line of the image (the width of the image in pixels).</span></span> <span data-ttu-id="6d1ff-552">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-552">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-553">Facoltativo per tutti gli elementi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-553">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-554">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-554">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <span data-ttu-id="6d1ff-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-556">Questa proprietà non è supportata in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-556">This property is not supported in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="6d1ff-557">Contiene le opzioni di compressione dei dati immagine.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-557">Contains image data packing options.</span></span> <span data-ttu-id="6d1ff-558">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-558">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-559">Un'applicazione legge questa proprietà per determinare le opzioni di compressione delle immagini o imposta le opzioni di compressione delle immagini correnti.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-559">An application reads this property to determine the image packing options or sets the current image packing options.</span></span></p>
<p><span data-ttu-id="6d1ff-560">Tipo: <strong>VT_I4</strong>; Accesso: lettura/scrittura; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-560">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="6d1ff-561">Se il dispositivo può essere impostato su un solo valore, creare un tipo di WIA_PROP_LIST e inserire il valore valido al suo interno.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-561">If the device can be set to only a single value, create a WIA_PROP_LIST type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="6d1ff-562">Nella tabella seguente sono riportate le due costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-562">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6d1ff-563">valore</span><span class="sxs-lookup"><span data-stu-id="6d1ff-563">Value</span></span></th>
<th><span data-ttu-id="6d1ff-564">Definizione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-564">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d1ff-565">WIA_PACKED_PIXEL</span><span class="sxs-lookup"><span data-stu-id="6d1ff-565">WIA_PACKED_PIXEL</span></span></td>
<td><span data-ttu-id="6d1ff-566">I dati dell'immagine sono in formato pixel compresso.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-566">Image data is in packed-pixel format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-567">WIA_PLANAR</span><span class="sxs-lookup"><span data-stu-id="6d1ff-567">WIA_PLANAR</span></span></td>
<td><span data-ttu-id="6d1ff-568">I dati dell'immagine sono in formato planare.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-568">Image data is in planar format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <span data-ttu-id="6d1ff-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-570">Contiene il formato preferito per le immagini che questo minidriver trasferisce.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-570">Contains the preferred format for images that this minidriver transfers.</span></span> <span data-ttu-id="6d1ff-571">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-571">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-572">Obbligatorio per tutti gli elementi WIA 2,0 abilitati per il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-572">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-573">Tipo: <strong>CLSID</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-573">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <span data-ttu-id="6d1ff-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-575">Specifica un CLSID che rappresenta un set di valori di proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-575">Specifies a CLSID that represents a set of device property values.</span></span> <span data-ttu-id="6d1ff-576">Se un driver di dispositivo implementa questa funzionalità, le applicazioni usano questa proprietà per determinare se il dispositivo supporta un set di valori.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-576">If a device driver implements this feature, applications use this property to determine if the device supports a set of values.</span></span></p>
<p><span data-ttu-id="6d1ff-577">Tipo: <strong>CLSID</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-577">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="6d1ff-578">La tabella seguente contiene le 12 costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-578">The following table has the 12 constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6d1ff-579">valore</span><span class="sxs-lookup"><span data-stu-id="6d1ff-579">Value</span></span></th>
<th><span data-ttu-id="6d1ff-580">Definizione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-580">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d1ff-581">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="6d1ff-581">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="6d1ff-582">Bitmap MicrosoftWindows con un file di intestazione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-582">MicrosoftWindows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-583">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-583">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="6d1ff-584">Metafile Windows esteso</span><span class="sxs-lookup"><span data-stu-id="6d1ff-584">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-585">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-585">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="6d1ff-586">Formato file scambiabile</span><span class="sxs-lookup"><span data-stu-id="6d1ff-586">Exchangeable File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-587">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="6d1ff-587">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="6d1ff-588">Formato FlashPix</span><span class="sxs-lookup"><span data-stu-id="6d1ff-588">FlashPix format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-589">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-589">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="6d1ff-590">Formato immagine GIF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-590">GIF image format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-591">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="6d1ff-591">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="6d1ff-592">Formato file icona Windows</span><span class="sxs-lookup"><span data-stu-id="6d1ff-592">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-593">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="6d1ff-593">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="6d1ff-594">Formato compresso JPEG</span><span class="sxs-lookup"><span data-stu-id="6d1ff-594">JPEG compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-595">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="6d1ff-595">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="6d1ff-596">Formato di file Eastman Kodak</span><span class="sxs-lookup"><span data-stu-id="6d1ff-596">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-597">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="6d1ff-597">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="6d1ff-598">Formato PNG W3C</span><span class="sxs-lookup"><span data-stu-id="6d1ff-598">W3C PNG format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-599">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="6d1ff-599">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="6d1ff-600">Bitmap di Windows senza un file di intestazione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-600">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-601">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-601">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="6d1ff-602">Tag Image File Format</span><span class="sxs-lookup"><span data-stu-id="6d1ff-602">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-603">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="6d1ff-603">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="6d1ff-604">Metafile di Windows</span><span class="sxs-lookup"><span data-stu-id="6d1ff-604">Windows metafile</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <span data-ttu-id="6d1ff-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-606">Supportato solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-606">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="6d1ff-607">Contiene il numero di bit in ogni canale.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-607">Contains the number of bits in each channel.</span></span> <span data-ttu-id="6d1ff-608">Questa proprietà deve essere segnalata come vettore di tutti i valori di BYTE quanti sono i canali, dove il primo BYTE corrisponde al numero di bit nel primo canale, il secondo byte al numero di bit nel secondo canale e così via.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-608">This property should be reported as a vector of as many BYTE values as there are channels, where the first BYTE corresponds to the number of bits in the first channel, the second byte to the number of bits in the second channel and so on.</span></span> <span data-ttu-id="6d1ff-609">È necessario che siano presenti tutti i canali in base ai WIA_IPA_CHANNELS_PER_PIXEL.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-609">There need to be as many entries as there are channels according to WIA_IPA_CHANNELS_PER_PIXEL.</span></span> <span data-ttu-id="6d1ff-610">Il driver imposta la proprietà quando l'applicazione passa a WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-610">The driver sets that property when the application switches to WiaImgFmt_RAW.</span></span> <span data-ttu-id="6d1ff-611">Per i sottotipi noti, il numero di voci elencate nella tabella è WIA_IPA_RAW_SUBTYPE.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-611">For the well-known subtypes, there are as many entries as listed in the table under WIA_IPA_RAW_SUBTYPE.</span></span></p>
<p><span data-ttu-id="6d1ff-612">Tipo: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-612">Type: <strong>VT_UI1</strong>|<strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <span data-ttu-id="6d1ff-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-614">Questa proprietà è riservata da per un utilizzo futuro e non è implementata in questo momento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-614">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="6d1ff-615">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-615">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <span data-ttu-id="6d1ff-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-617">Specifica se visualizzare le pagine delle proprietà generali per gli elementi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-617">Specifies whether to suppress the general property pages for items on the device.</span></span></p>
<p><span data-ttu-id="6d1ff-618">Questa proprietà è disponibile in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-618">This property is available on Windows XP and later.</span></span></p>
<p><span data-ttu-id="6d1ff-619">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-619">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="6d1ff-620">La tabella seguente contiene le costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-620">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="6d1ff-621">L'asterisco \* indica che la costante non è valida con Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-621">The asterisk \* indicates that the constant is not valid with Windows Vista and later.</span></span> <span data-ttu-id="6d1ff-622">È disponibile solo tramite l'interfaccia <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-622">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6d1ff-623">Costante</span><span class="sxs-lookup"><span data-stu-id="6d1ff-623">Constant</span></span></th>
<th><span data-ttu-id="6d1ff-624">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-624">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d1ff-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL \*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL\*</span></span></td>
<td><span data-ttu-id="6d1ff-626">Non visualizzare la pagina delle proprietà elemento generale per una fotocamera.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-626">Suppress the general item property page for a camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span><span class="sxs-lookup"><span data-stu-id="6d1ff-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span></span></td>
<td><span data-ttu-id="6d1ff-628">Non visualizzare la pagina delle proprietà elemento generale per uno scanner.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-628">Suppress the general item property page for a scanner.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <span data-ttu-id="6d1ff-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-630">Questa proprietà contiene l'impostazione del metodo di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-630">This property contains the transfer method setting.</span></span> <span data-ttu-id="6d1ff-631">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-631">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6d1ff-632">Un'applicazione legge questa proprietà per determinare il metodo di trasferimento dei dati del minidriver.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-632">An application reads this property to determine the minidriver's method of data transfer.</span></span></p>
<p><span data-ttu-id="6d1ff-633">Obbligatorio per tutti gli elementi WIA 2,0 abilitati per il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-633">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="6d1ff-634">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-634">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="6d1ff-635">La tabella seguente contiene le costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-635">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="6d1ff-636">L'asterisco \* indica costanti non valide con Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-636">The asterisk \* indicates constants that are not valid with Windows Vista and later.</span></span> <span data-ttu-id="6d1ff-637">Sono disponibili solo tramite l'interfaccia <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6d1ff-637">(They are only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6d1ff-638">Tipo di trasferimento</span><span class="sxs-lookup"><span data-stu-id="6d1ff-638">Transfer Type</span></span></th>
<th><span data-ttu-id="6d1ff-639">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-639">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d1ff-640">TYMED_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-640">TYMED_CALLBACK\*</span></span></td>
<td><span data-ttu-id="6d1ff-641">Trasferire un'immagine in memoria, in bande.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-641">Transfer an image to memory, in bands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-642">TYMED_MULTIPAGE_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="6d1ff-642">TYMED_MULTIPAGE_CALLBACK\*</span></span></td>
<td><span data-ttu-id="6d1ff-643">Trasferire più immagini in memoria, in bande.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-643">Transfer multiple images to memory, in bands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d1ff-644">TYMED_FILE</span><span class="sxs-lookup"><span data-stu-id="6d1ff-644">TYMED_FILE</span></span></td>
<td><span data-ttu-id="6d1ff-645">Trasferire un'immagine in un file.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-645">Transfer an image to a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d1ff-646">TYMED_MULTIPAGE_FILE</span><span class="sxs-lookup"><span data-stu-id="6d1ff-646">TYMED_MULTIPAGE_FILE</span></span></td>
<td><span data-ttu-id="6d1ff-647">Trasferire un'immagine in un file.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-647">Transfer an image to a file.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="6d1ff-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </span><span class="sxs-lookup"><span data-stu-id="6d1ff-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6d1ff-649">Supportato solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-649">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="6d1ff-650">Specifica il numero di byte da caricare per un elemento.</span><span class="sxs-lookup"><span data-stu-id="6d1ff-650">Specifies the number of bytes to upload for an item.</span></span></p>
<p><span data-ttu-id="6d1ff-651">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6d1ff-651">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="6d1ff-652">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d1ff-652">Requirements</span></span>



| <span data-ttu-id="6d1ff-653">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d1ff-653">Requirement</span></span> | <span data-ttu-id="6d1ff-654">Valore</span><span class="sxs-lookup"><span data-stu-id="6d1ff-654">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6d1ff-655">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d1ff-655">Minimum supported client</span></span><br/> | <span data-ttu-id="6d1ff-656">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d1ff-656">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6d1ff-657">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d1ff-657">Minimum supported server</span></span><br/> | <span data-ttu-id="6d1ff-658">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6d1ff-658">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6d1ff-659">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d1ff-659">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d1ff-660"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d1ff-660"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




