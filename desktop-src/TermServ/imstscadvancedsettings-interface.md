---
title: Interfaccia IMsTscAdvancedSettings
description: Include metodi per recuperare e impostare le proprietà che abilitano la memorizzazione nella cache, la compressione e il reindirizzamento degli Appunti e della stampante bitmap.
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4d55df30c940ecc5a5515f13c05a285507499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301626"
---
# <a name="imstscadvancedsettings-interface"></a><span data-ttu-id="9239b-105">Interfaccia IMsTscAdvancedSettings</span><span class="sxs-lookup"><span data-stu-id="9239b-105">IMsTscAdvancedSettings interface</span></span>

<span data-ttu-id="9239b-106">Include metodi per recuperare e impostare le proprietà che abilitano la memorizzazione nella cache, la compressione e il reindirizzamento degli Appunti e della stampante bitmap.</span><span class="sxs-lookup"><span data-stu-id="9239b-106">Includes methods to retrieve and set properties that enable bitmap caching, compression, and printer and clipboard redirection.</span></span> <span data-ttu-id="9239b-107">È anche possibile specificare i nomi delle dll client del canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="9239b-107">You can also specify names of virtual channel client DLLs.</span></span>

<span data-ttu-id="9239b-108">Per ottenere un'istanza di questa interfaccia, è possibile usare la proprietà [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="9239b-108">You obtain an instance of this interface by using the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="9239b-109">Membri</span><span class="sxs-lookup"><span data-stu-id="9239b-109">Members</span></span>

<span data-ttu-id="9239b-110">L'interfaccia **IMsTscAdvancedSettings** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="9239b-110">The **IMsTscAdvancedSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9239b-111">**IMsTscAdvancedSettings** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9239b-111">**IMsTscAdvancedSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="9239b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9239b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9239b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9239b-113">Properties</span></span>

<span data-ttu-id="9239b-114">L'interfaccia **IMsTscAdvancedSettings** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9239b-114">The **IMsTscAdvancedSettings** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="9239b-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9239b-115">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="9239b-116">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="9239b-116">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="9239b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9239b-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="9239b-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a></span><span class="sxs-lookup"><span data-stu-id="9239b-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="9239b-119">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-120">Specifica se la modalità di input in background è abilitata.</span><span class="sxs-lookup"><span data-stu-id="9239b-120">Specifies whether background input mode is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="9239b-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a></span><span class="sxs-lookup"><span data-stu-id="9239b-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="9239b-122">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-123">Specifica se la memorizzazione nella cache bitmap è abilitata.</span><span class="sxs-lookup"><span data-stu-id="9239b-123">Specifies whether bitmap caching is enabled.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9239b-124">L'errore di ortografia nel nome della proprietà si trova nella versione rilasciata del controllo.</span><span class="sxs-lookup"><span data-stu-id="9239b-124">The spelling error in the name of the property is in the released version of the control.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="9239b-125"><a href="imstscadvancedsettings-compress.md"><strong>Comprimere</strong></a></span><span class="sxs-lookup"><span data-stu-id="9239b-125"><a href="imstscadvancedsettings-compress.md"><strong>Compress</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="9239b-126">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-127">Specifica se la compressione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="9239b-127">Specifies whether compression is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="9239b-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a></span><span class="sxs-lookup"><span data-stu-id="9239b-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="9239b-129">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-130">Specifica se la modalità a schermo intero gestita dal contenitore è abilitata.</span><span class="sxs-lookup"><span data-stu-id="9239b-130">Specifies whether the container-handled full-screen mode is enabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="9239b-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a></span><span class="sxs-lookup"><span data-stu-id="9239b-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-132">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="9239b-132">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-133">Specifica se il reindirizzamento della stampante e degli Appunti è abilitato.</span><span class="sxs-lookup"><span data-stu-id="9239b-133">Specifies whether printer and clipboard redirection is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="9239b-134"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="9239b-134"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-135">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="9239b-135">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-136">Specifica il nome del file che contiene i dati dell'icona a cui sarà possibile accedere quando viene visualizzato il client in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="9239b-136">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="9239b-137"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a></span><span class="sxs-lookup"><span data-stu-id="9239b-137"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-138">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="9239b-138">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-139">Specifica l'indice dell'icona all'interno del file icona corrente.</span><span class="sxs-lookup"><span data-stu-id="9239b-139">Specifies the index of the icon within the current icon file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="9239b-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="9239b-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-141">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="9239b-141">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-142">Specifica il nome dell'identificatore delle impostazioni locali di input attivo (denominato in precedenza il layout della tastiera) da usare per la connessione.</span><span class="sxs-lookup"><span data-stu-id="9239b-142">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="9239b-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a></span><span class="sxs-lookup"><span data-stu-id="9239b-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-144">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="9239b-144">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="9239b-145">Specifica i nomi delle dll client del canale virtuale da caricare.</span><span class="sxs-lookup"><span data-stu-id="9239b-145">Specifies the names of virtual channel client DLLs to be loaded.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="9239b-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="9239b-146">Remarks</span></span>

<span data-ttu-id="9239b-147">Questa interfaccia è stata estesa dalle interfacce seguenti, in cui ogni nuova interfaccia eredita tutti i metodi e le proprietà delle interfacce precedenti:</span><span class="sxs-lookup"><span data-stu-id="9239b-147">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="9239b-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="9239b-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
-   [<span data-ttu-id="9239b-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="9239b-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
-   [<span data-ttu-id="9239b-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9239b-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
-   [<span data-ttu-id="9239b-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9239b-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="9239b-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9239b-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="9239b-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9239b-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="9239b-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9239b-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="9239b-155">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9239b-155">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9239b-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9239b-156">Requirements</span></span>



| <span data-ttu-id="9239b-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="9239b-157">Requirement</span></span> | <span data-ttu-id="9239b-158">Valore</span><span class="sxs-lookup"><span data-stu-id="9239b-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9239b-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9239b-159">Minimum supported client</span></span><br/> | <span data-ttu-id="9239b-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9239b-160">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="9239b-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9239b-161">Minimum supported server</span></span><br/> | <span data-ttu-id="9239b-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9239b-162">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="9239b-163">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9239b-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="9239b-164"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9239b-164"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="9239b-165">DLL</span><span class="sxs-lookup"><span data-stu-id="9239b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9239b-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9239b-166"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="9239b-167">IID</span><span class="sxs-lookup"><span data-stu-id="9239b-167">IID</span></span><br/>                      | <span data-ttu-id="9239b-168">IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="9239b-168">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9239b-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9239b-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9239b-170">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="9239b-170">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="9239b-171">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9239b-171">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

