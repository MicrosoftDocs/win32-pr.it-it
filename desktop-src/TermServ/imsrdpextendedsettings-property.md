---
title: Proprietà della proprietà IMsRdpExtendedSettings
description: Contiene una proprietà denominata.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Proprietà Servizi Desktop remoto proprietà
- Servizi Desktop remoto proprietà proprietà, interfaccia IMsRdpExtendedSettings
- Interfaccia IMsRdpExtendedSettings Servizi Desktop remoto, proprietà Property
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc8ce59e5a2bd50a4e61ad75b5124b24c21b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "103745351"
---
# <a name="imsrdpextendedsettingsproperty-property"></a><span data-ttu-id="9670a-106">IMsRdpExtendedSettings::P proprietà roperty</span><span class="sxs-lookup"><span data-stu-id="9670a-106">IMsRdpExtendedSettings::Property property</span></span>

<span data-ttu-id="9670a-107">Contiene una proprietà denominata.</span><span class="sxs-lookup"><span data-stu-id="9670a-107">Contains a named property.</span></span>

<span data-ttu-id="9670a-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9670a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9670a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9670a-109">Syntax</span></span>


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a><span data-ttu-id="9670a-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9670a-110">Property value</span></span>

<span data-ttu-id="9670a-111">Valore della proprietà denominata.</span><span class="sxs-lookup"><span data-stu-id="9670a-111">The named property value.</span></span>

| <span data-ttu-id="9670a-112">Nome proprietà</span><span class="sxs-lookup"><span data-stu-id="9670a-112">Property name</span></span> | <span data-ttu-id="9670a-113">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9670a-113">Data type</span></span> | <span data-ttu-id="9670a-114">Access</span><span class="sxs-lookup"><span data-stu-id="9670a-114">Access</span></span> | <span data-ttu-id="9670a-115">Può essere modificato dopo l'avvio della connessione</span><span class="sxs-lookup"><span data-stu-id="9670a-115">Can be changed after connection started</span></span> | <span data-ttu-id="9670a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9670a-116">Description</span></span> |
|----------|-----------|--------|-----------------------------------------|-------------|
| <span data-ttu-id="9670a-117">ConnectToChildSession</span><span class="sxs-lookup"><span data-stu-id="9670a-117">ConnectToChildSession</span></span> | <span data-ttu-id="9670a-118">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="9670a-118">**VT\_BOOL**</span></span> | <span data-ttu-id="9670a-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="9670a-119">Read/Write</span></span> | <span data-ttu-id="9670a-120">Sì</span><span class="sxs-lookup"><span data-stu-id="9670a-120">Yes</span></span> | <span data-ttu-id="9670a-121">Impostando questa proprietà su **true** , il controllo client si connette alla sessione figlio nel computer locale anziché in un server remoto.</span><span class="sxs-lookup"><span data-stu-id="9670a-121">Setting this property to **True** causes the client control to connect to the child session on the local machine instead of a remote server.</span></span> <span data-ttu-id="9670a-122">Se questa proprietà è impostata su **true**, non è possibile connettersi a un server remoto perché tutte le connessioni vengono reindirizzate a localhost.</span><span class="sxs-lookup"><span data-stu-id="9670a-122">If this property is set to **true**, you cannot connect to a remote server because all connections are redirected to localhost.</span></span> <span data-ttu-id="9670a-123">Per ulteriori informazioni sulle sessioni figlio, vedere [sessioni figlio](child-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="9670a-123">For more information about child sessions, see [Child Sessions](child-sessions.md).</span></span> |
| <span data-ttu-id="9670a-124">DisableCredentialsDelegation</span><span class="sxs-lookup"><span data-stu-id="9670a-124">DisableCredentialsDelegation</span></span> | <span data-ttu-id="9670a-125">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="9670a-125">**VT\_BOOL**</span></span> | <span data-ttu-id="9670a-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="9670a-126">Read/Write</span></span> | <span data-ttu-id="9670a-127">No</span><span class="sxs-lookup"><span data-stu-id="9670a-127">No</span></span> | <span data-ttu-id="9670a-128">Se **true**, le credenziali non vengono inviate al server remoto.</span><span class="sxs-lookup"><span data-stu-id="9670a-128">If **True**, credentials are not sent to the remote server.</span></span> |
| <span data-ttu-id="9670a-129">EnableFrameBufferRedirection</span><span class="sxs-lookup"><span data-stu-id="9670a-129">EnableFrameBufferRedirection</span></span> | <span data-ttu-id="9670a-130">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="9670a-130">**VT\_BOOL**</span></span> | <span data-ttu-id="9670a-131">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="9670a-131">Read/Write</span></span> | <span data-ttu-id="9670a-132">No</span><span class="sxs-lookup"><span data-stu-id="9670a-132">No</span></span> | <span data-ttu-id="9670a-133">Se **true**, viene eseguito un tentativo di reindirizzamento del buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="9670a-133">If **True**, frame buffer redirection is attempted.</span></span> <span data-ttu-id="9670a-134">Per una connessione loopback (lo stesso computer è sia client che Server), il reindirizzamento del buffer dei frame consente la condivisione della memoria per il buffer dei frame tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="9670a-134">For a loopback connection (the same computer is both client and server) frame buffer redirection allows the memory for the frame buffer to be shared between the sessions.</span></span> |
| <span data-ttu-id="9670a-135">EnableHardwareMode</span><span class="sxs-lookup"><span data-stu-id="9670a-135">EnableHardwareMode</span></span> | <span data-ttu-id="9670a-136">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="9670a-136">**VT\_BOOL**</span></span>  | <span data-ttu-id="9670a-137">Solo scrittura</span><span class="sxs-lookup"><span data-stu-id="9670a-137">Write Only</span></span> | <span data-ttu-id="9670a-138">No</span><span class="sxs-lookup"><span data-stu-id="9670a-138">No</span></span> | <span data-ttu-id="9670a-139">Se **true**, viene effettuato un tentativo di assistenza hardware con la decodifica grafica.</span><span class="sxs-lookup"><span data-stu-id="9670a-139">If **True**, hardware assist with graphics decoding is attempted.</span></span> |
| <span data-ttu-id="9670a-140">IgnoreCursors</span><span class="sxs-lookup"><span data-stu-id="9670a-140">IgnoreCursors</span></span> | <span data-ttu-id="9670a-141">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="9670a-141">**VT\_BOOL**</span></span> | <span data-ttu-id="9670a-142">Solo scrittura</span><span class="sxs-lookup"><span data-stu-id="9670a-142">Write Only</span></span> | <span data-ttu-id="9670a-143">No</span><span class="sxs-lookup"><span data-stu-id="9670a-143">No</span></span> | <span data-ttu-id="9670a-144">Se **true**, i cursori inviati dal server remoto vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="9670a-144">If **True**, cursors sent by the remote server are ignored.</span></span> |
| <span data-ttu-id="9670a-145">ManualClipboardSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="9670a-145">ManualClipboardSyncEnabled</span></span> | <span data-ttu-id="9670a-146">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="9670a-146">**VT\_BOOL**</span></span> | <span data-ttu-id="9670a-147">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="9670a-147">Read/Write</span></span> | <span data-ttu-id="9670a-148">Sì</span><span class="sxs-lookup"><span data-stu-id="9670a-148">Yes</span></span> | <span data-ttu-id="9670a-149">L'impostazione di questa proprietà su **true** indica che gli Appunti locali e remoti non verranno mantenuti sincronizzati automaticamente. È invece necessario utilizzare l'interfaccia [**IMsRdpClipboard**](imsrdpclipboard.md) per sincronizzare i formati degli Appunti dagli Appunti locali negli Appunti remoti e negli Appunti remoti negli Appunti locali.</span><span class="sxs-lookup"><span data-stu-id="9670a-149">Setting this property to **True** means that the local and remote clipboards will not be automatically kept in sync. Instead the [**IMsRdpClipboard**](imsrdpclipboard.md) interface must be used to sync clipboard formats from the local clipboard to the remote clipboard and the remote clipboard to the local clipboard.</span></span> |
| <span data-ttu-id="9670a-150">ZoomLevel</span><span class="sxs-lookup"><span data-stu-id="9670a-150">ZoomLevel</span></span> | <span data-ttu-id="9670a-151">\**_\_UI4 VT_*</span><span class="sxs-lookup"><span data-stu-id="9670a-151">\**_VT\_UI4_*</span></span> | <span data-ttu-id="9670a-152">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="9670a-152">Read/Write</span></span> | <span data-ttu-id="9670a-153">Sì</span><span class="sxs-lookup"><span data-stu-id="9670a-153">Yes</span></span> | <span data-ttu-id="9670a-154">Implementa la funzionalità di zoom utilizzando il controllo ActiveX RDP.</span><span class="sxs-lookup"><span data-stu-id="9670a-154">Implements the Zoom feature by using the RDP ActiveX control.</span></span> <span data-ttu-id="9670a-155">La funzionalità di zoom è disponibile dal menu di **sistema** di RDP.</span><span class="sxs-lookup"><span data-stu-id="9670a-155">The Zoom feature is available from the **System** menu of RDP.</span></span> <span data-ttu-id="9670a-156">La proprietà **ZoomLevel** non ha alcun effetto in modalità RemoteApp e in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="9670a-156">The **ZoomLevel** property has no effect in RemoteApp mode and full-screen mode.</span></span> <span data-ttu-id="9670a-157">[**IMsRdpClientAdvancedSettings:: SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) e **ZoomLevel** si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="9670a-157">[**IMsRdpClientAdvancedSettings::SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) and **ZoomLevel** are mutually exclusive.</span></span> |

## <a name="requirements"></a><span data-ttu-id="9670a-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9670a-158">Requirements</span></span>



| <span data-ttu-id="9670a-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="9670a-159">Requirement</span></span> | <span data-ttu-id="9670a-160">Valore</span><span class="sxs-lookup"><span data-stu-id="9670a-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9670a-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9670a-161">Minimum supported client</span></span><br/> | <span data-ttu-id="9670a-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9670a-162">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9670a-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9670a-163">Minimum supported server</span></span><br/> | <span data-ttu-id="9670a-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9670a-164">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9670a-165">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9670a-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="9670a-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9670a-166"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="9670a-167">DLL</span><span class="sxs-lookup"><span data-stu-id="9670a-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9670a-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9670a-168"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="9670a-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="9670a-169">CLSID</span></span><br/>                    | <span data-ttu-id="9670a-170">CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54d38bf7-b1ef-4479-9674-1bd6ea465258</span><span class="sxs-lookup"><span data-stu-id="9670a-170">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54d38bf7-b1ef-4479-9674-1bd6ea465258</span></span><br/> <span data-ttu-id="9670a-171">CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041d-42e3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="9670a-171">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="9670a-172">CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="9670a-172">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="9670a-173">IID</span><span class="sxs-lookup"><span data-stu-id="9670a-173">IID</span></span><br/>                      | <span data-ttu-id="9670a-174">IID \_ IMsRdpExtendedSettings è definito come 302D8188-0052-4807-806A-362B628F9AC5</span><span class="sxs-lookup"><span data-stu-id="9670a-174">IID\_IMsRdpExtendedSettings is defined as 302D8188-0052-4807-806A-362B628F9AC5</span></span><br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a><span data-ttu-id="9670a-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9670a-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9670a-176">**IMsRdpExtendedSettings**</span><span class="sxs-lookup"><span data-stu-id="9670a-176">**IMsRdpExtendedSettings**</span></span>](imsrdpextendedsettings.md)
</dt> </dl>

 

 





