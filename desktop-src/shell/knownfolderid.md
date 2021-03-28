---
Description: Le costanti KNOWNFOLDERID rappresentano i GUID che identificano le cartelle standard registrate con il sistema come cartelle note.
ms.assetid: f2c08ade-3083-44e4-82b0-dde45f0e3094
title: KNOWNFOLDERID (KnownFolders. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 97748d074d6b0982708f51ea679f0629e8abfad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982859"
---
# <a name="knownfolderid"></a><span data-ttu-id="9c198-103">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-103">KNOWNFOLDERID</span></span>

<span data-ttu-id="9c198-104">Le costanti **KNOWNFOLDERID** rappresentano i GUID che identificano le cartelle standard registrate con il sistema come [cartelle note](known-folders.md).</span><span class="sxs-lookup"><span data-stu-id="9c198-104">The **KNOWNFOLDERID** constants represent GUIDs that identify standard folders registered with the system as [Known Folders](known-folders.md).</span></span> <span data-ttu-id="9c198-105">Queste cartelle vengono installate con Windows Vista e sistemi operativi successivi e un computer avrà solo le cartelle appropriate per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9c198-105">These folders are installed with Windows Vista and later operating systems, and a computer will have only folders appropriate to it installed.</span></span> <span data-ttu-id="9c198-106">Per le descrizioni di queste cartelle, vedere [**CSIDL**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="9c198-106">For descriptions of these folders, see [**CSIDL**](csidl.md).</span></span>

## <a name="example"></a><span data-ttu-id="9c198-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="9c198-107">Example</span></span>

```c
HRESULT CExplorerBrowserHostDialog::_FillViewWithKnownFolders(IResultsFolder *prf)
{
    IKnownFolderManager *pManager;
    HRESULT hr = CoCreateInstance(CLSID_KnownFolderManager, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pManager));
    if (SUCCEEDED(hr))
    {
        UINT cCount;
        KNOWNFOLDERID *pkfid;

        hr = pManager->GetFolderIds(&pkfid, &cCount);
        if (SUCCEEDED(hr))
        {
            for (UINT i = 0; i < cCount; i++)
            {
                IKnownFolder *pKnownFolder;
                hr = pManager->GetFolder(pkfid[i], &pKnownFolder);
                if (SUCCEEDED(hr))
                {
                    IShellItem *psi;
                    hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                    if (SUCCEEDED(hr))
                    {
                        hr = prf->AddItem(psi);
                        psi->Release();
                    }
                    pKnownFolder->Release();
                }
            }
            CoTaskMemFree(pkfid);
        }
        pManager->Release();
    }
    return hr;
}

```

<span data-ttu-id="9c198-108">Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="9c198-108">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="9c198-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="9c198-109">Constants</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="9c198-110">Costante</span><span class="sxs-lookup"><span data-stu-id="9c198-110">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="9c198-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c198-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AccountPictures"></span><span id="folderid_accountpictures"></span><span id="FOLDERID_ACCOUNTPICTURES"></span><dl> <span data-ttu-id="9c198-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-113">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-113">GUID</span></span></td>
<td><span data-ttu-id="9c198-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span><span class="sxs-lookup"><span data-stu-id="9c198-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-115">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-115">Display Name</span></span></td>
<td><span data-ttu-id="9c198-116">Immagini account</span><span class="sxs-lookup"><span data-stu-id="9c198-116">Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-117">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-117">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-118">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-118">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-119">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-119">Default Path</span></span></td>
<td><span data-ttu-id="9c198-120">%APPDATA%\Microsoft\Windows\AccountPictures</span><span class="sxs-lookup"><span data-stu-id="9c198-120">%APPDATA%\Microsoft\Windows\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-121">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-121">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-122">None, valore introdotto in Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c198-122">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-123">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-123">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-124">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-124">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-125">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-125">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-126">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-126">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AddNewPrograms"></span><span id="folderid_addnewprograms"></span><span id="FOLDERID_ADDNEWPROGRAMS"></span><dl> <span data-ttu-id="9c198-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-128">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-128">GUID</span></span></td>
<td><span data-ttu-id="9c198-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span><span class="sxs-lookup"><span data-stu-id="9c198-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-130">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-130">Display Name</span></span></td>
<td><span data-ttu-id="9c198-131">Ottieni programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-131">Get Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-132">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-132">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-133">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-133">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-134">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-134">Default Path</span></span></td>
<td><span data-ttu-id="9c198-135">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-135">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-136">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-136">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-137">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-137">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-138">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-138">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-139">Aggiungere nuovi programmi (disponibili nell'elemento <strong>Installazione applicazioni</strong> nel pannello di controllo)</span><span class="sxs-lookup"><span data-stu-id="9c198-139">Add New Programs (found in the <strong>Add or Remove Programs</strong> item in the Control Panel)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-140">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-140">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-141">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-141">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AdminTools"></span><span id="folderid_admintools"></span><span id="FOLDERID_ADMINTOOLS"></span><dl> <span data-ttu-id="9c198-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-143">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-143">GUID</span></span></td>
<td><span data-ttu-id="9c198-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span><span class="sxs-lookup"><span data-stu-id="9c198-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-145">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-145">Display Name</span></span></td>
<td><span data-ttu-id="9c198-146">Strumenti di amministrazione</span><span class="sxs-lookup"><span data-stu-id="9c198-146">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-147">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-147">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-148">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-148">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-149">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-149">Default Path</span></span></td>
<td><span data-ttu-id="9c198-150">Strumenti Avvio\Programmi\Strumenti%APPDATA%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="9c198-150">%APPDATA%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-151">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-151">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-152">CSIDL_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="9c198-152">CSIDL_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-153">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-153">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-154">Strumenti di amministrazione</span><span class="sxs-lookup"><span data-stu-id="9c198-154">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-155">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-155">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-156">Strumenti Avvio\Programmi\Strumenti%USERPROFILE%\Menu</span><span class="sxs-lookup"><span data-stu-id="9c198-156">%USERPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataDesktop"></span><span id="folderid_appdatadesktop"></span><span id="FOLDERID_APPDATADESKTOP"></span><dl> <span data-ttu-id="9c198-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-158">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-158">GUID</span></span></td>
<td><span data-ttu-id="9c198-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span><span class="sxs-lookup"><span data-stu-id="9c198-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-160">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-160">Display Name</span></span></td>
<td><span data-ttu-id="9c198-161">AppDataDesktop</span><span class="sxs-lookup"><span data-stu-id="9c198-161">AppDataDesktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-162">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-162">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-163">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-163">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-164">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-164">Default Path</span></span></td>
<td><span data-ttu-id="9c198-165">%LOCALAPPDATA%\Desktop</span><span class="sxs-lookup"><span data-stu-id="9c198-165">%LOCALAPPDATA%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-166">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-166">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-167">None, valore introdotto in Windows 10, versione 1709</span><span class="sxs-lookup"><span data-stu-id="9c198-167">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-168">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-168">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-169">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-169">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-170">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-170">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-171">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-171">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="9c198-172">Questo FOLDERID viene usato internamente dalle applicazioni .NET per abilitare la funzionalità dell'app multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="9c198-172">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="9c198-173">Non è destinato a essere usato direttamente da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c198-173">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataDocuments"></span><span id="folderid_appdatadocuments"></span><span id="FOLDERID_APPDATADOCUMENTS"></span><dl> <span data-ttu-id="9c198-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-175">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-175">GUID</span></span></td>
<td><span data-ttu-id="9c198-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span><span class="sxs-lookup"><span data-stu-id="9c198-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-177">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-177">Display Name</span></span></td>
<td><span data-ttu-id="9c198-178">AppDataDocuments</span><span class="sxs-lookup"><span data-stu-id="9c198-178">AppDataDocuments</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-179">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-179">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-180">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-180">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-181">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-181">Default Path</span></span></td>
<td><span data-ttu-id="9c198-182">%LOCALAPPDATA%\Documents</span><span class="sxs-lookup"><span data-stu-id="9c198-182">%LOCALAPPDATA%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-183">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-183">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-184">None, valore introdotto in Windows 10, versione 1709</span><span class="sxs-lookup"><span data-stu-id="9c198-184">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-185">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-185">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-186">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-186">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-187">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-187">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-188">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-188">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="9c198-189">Questo FOLDERID viene usato internamente dalle applicazioni .NET per abilitare la funzionalità dell'app multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="9c198-189">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="9c198-190">Non è destinato a essere usato direttamente da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c198-190">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataFavorites"></span><span id="folderid_appdatafavorites"></span><span id="FOLDERID_APPDATAFAVORITES"></span><dl> <span data-ttu-id="9c198-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-192">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-192">GUID</span></span></td>
<td><span data-ttu-id="9c198-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span><span class="sxs-lookup"><span data-stu-id="9c198-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-194">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-194">Display Name</span></span></td>
<td><span data-ttu-id="9c198-195">AppDataFavorites</span><span class="sxs-lookup"><span data-stu-id="9c198-195">AppDataFavorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-196">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-196">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-197">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-197">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-198">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-198">Default Path</span></span></td>
<td><span data-ttu-id="9c198-199">%LOCALAPPDATA%\Favorites</span><span class="sxs-lookup"><span data-stu-id="9c198-199">%LOCALAPPDATA%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-200">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-200">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-201">None, valore introdotto in Windows 10, versione 1709</span><span class="sxs-lookup"><span data-stu-id="9c198-201">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-202">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-202">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-203">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-203">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-204">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-204">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-205">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-205">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="9c198-206">Questo FOLDERID viene usato internamente dalle applicazioni .NET per abilitare la funzionalità dell'app multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="9c198-206">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="9c198-207">Non è destinato a essere usato direttamente da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c198-207">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataProgramData"></span><span id="folderid_appdataprogramdata"></span><span id="FOLDERID_APPDATAPROGRAMDATA"></span><dl> <span data-ttu-id="9c198-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-209">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-209">GUID</span></span></td>
<td><span data-ttu-id="9c198-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span><span class="sxs-lookup"><span data-stu-id="9c198-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-211">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-211">Display Name</span></span></td>
<td><span data-ttu-id="9c198-212">AppDataProgramData</span><span class="sxs-lookup"><span data-stu-id="9c198-212">AppDataProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-213">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-213">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-214">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-214">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-215">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-215">Default Path</span></span></td>
<td><span data-ttu-id="9c198-216">%LOCALAPPDATA%\ProgramData</span><span class="sxs-lookup"><span data-stu-id="9c198-216">%LOCALAPPDATA%\ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-217">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-217">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-218">None, valore introdotto in Windows 10, versione 1709</span><span class="sxs-lookup"><span data-stu-id="9c198-218">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-219">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-219">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-220">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-220">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-221">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-221">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-222">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-222">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="9c198-223">Questo FOLDERID viene usato internamente dalle applicazioni .NET per abilitare la funzionalità dell'app multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="9c198-223">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="9c198-224">Non è destinato a essere usato direttamente da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c198-224">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ApplicationShortcuts"></span><span id="folderid_applicationshortcuts"></span><span id="FOLDERID_APPLICATIONSHORTCUTS"></span><dl> <span data-ttu-id="9c198-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-226">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-226">GUID</span></span></td>
<td><span data-ttu-id="9c198-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span><span class="sxs-lookup"><span data-stu-id="9c198-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-228">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-228">Display Name</span></span></td>
<td><span data-ttu-id="9c198-229">Collegamenti alle applicazioni</span><span class="sxs-lookup"><span data-stu-id="9c198-229">Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-230">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-230">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-231">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-231">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-232">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-232">Default Path</span></span></td>
<td><span data-ttu-id="9c198-233">Collegamenti%LOCALAPPDATA%\Microsoft\Windows\Application</span><span class="sxs-lookup"><span data-stu-id="9c198-233">%LOCALAPPDATA%\Microsoft\Windows\Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-234">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-234">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-235">None, valore introdotto in Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c198-235">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-236">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-236">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-237">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-237">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-238">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-238">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-239">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-239">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppsFolder"></span><span id="folderid_appsfolder"></span><span id="FOLDERID_APPSFOLDER"></span><dl> <span data-ttu-id="9c198-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-241">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-241">GUID</span></span></td>
<td><span data-ttu-id="9c198-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span><span class="sxs-lookup"><span data-stu-id="9c198-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-243">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-243">Display Name</span></span></td>
<td><span data-ttu-id="9c198-244">Applicazioni</span><span class="sxs-lookup"><span data-stu-id="9c198-244">Applications</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-245">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-245">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-246">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-246">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-247">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-247">Default Path</span></span></td>
<td><span data-ttu-id="9c198-248">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-248">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-249">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-249">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-250">None, valore introdotto in Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c198-250">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-251">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-251">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-252">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-252">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-253">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-253">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-254">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-254">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppUpdates"></span><span id="folderid_appupdates"></span><span id="FOLDERID_APPUPDATES"></span><dl> <span data-ttu-id="9c198-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-256">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-256">GUID</span></span></td>
<td><span data-ttu-id="9c198-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span><span class="sxs-lookup"><span data-stu-id="9c198-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-258">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-258">Display Name</span></span></td>
<td><span data-ttu-id="9c198-259">Aggiornamenti installati</span><span class="sxs-lookup"><span data-stu-id="9c198-259">Installed Updates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-260">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-260">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-261">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-261">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-262">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-262">Default Path</span></span></td>
<td><span data-ttu-id="9c198-263">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-263">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-264">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-264">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-265">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-265">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-266">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-266">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-267">None, valore introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9c198-267">None, value introduced in Windows Vista.</span></span> <span data-ttu-id="9c198-268">Nelle versioni precedenti di Windows le informazioni contenute in questa pagina sono state incluse in <strong>Installazione applicazioni</strong> se è stata selezionata la casella <strong>Mostra aggiornamenti</strong> .</span><span class="sxs-lookup"><span data-stu-id="9c198-268">In earlier versions of Windows, the information on this page was included in <strong>Add or Remove Programs</strong> if the <strong>Show updates</strong> box was checked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-269">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-269">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-270">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-270">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CameraRoll"></span><span id="folderid_cameraroll"></span><span id="FOLDERID_CAMERAROLL"></span><dl> <span data-ttu-id="9c198-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-272">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-272">GUID</span></span></td>
<td><span data-ttu-id="9c198-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span><span class="sxs-lookup"><span data-stu-id="9c198-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-274">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-274">Display Name</span></span></td>
<td><span data-ttu-id="9c198-275">Rullo della fotocamera</span><span class="sxs-lookup"><span data-stu-id="9c198-275">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-276">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-276">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-277">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-277">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-278">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-278">Default Path</span></span></td>
<td><span data-ttu-id="9c198-279">%USERPROFILE%\Pictures\Camera roll</span><span class="sxs-lookup"><span data-stu-id="9c198-279">%USERPROFILE%\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-280">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-280">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-281">None, valore introdotto in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9c198-281">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-282">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-282">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-283">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-283">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-284">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-284">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-285">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-285">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CDBurning"></span><span id="folderid_cdburning"></span><span id="FOLDERID_CDBURNING"></span><dl> <span data-ttu-id="9c198-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-287">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-287">GUID</span></span></td>
<td><span data-ttu-id="9c198-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span><span class="sxs-lookup"><span data-stu-id="9c198-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-289">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-289">Display Name</span></span></td>
<td><span data-ttu-id="9c198-290">Cartella di masterizzazione temporanea</span><span class="sxs-lookup"><span data-stu-id="9c198-290">Temporary Burn Folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-291">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-291">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-292">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-292">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-293">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-293">Default Path</span></span></td>
<td><span data-ttu-id="9c198-294">%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</span><span class="sxs-lookup"><span data-stu-id="9c198-294">%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-295">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-295">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-296">CSIDL_CDBURN_AREA</span><span class="sxs-lookup"><span data-stu-id="9c198-296">CSIDL_CDBURN_AREA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-297">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-297">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-298">Masterizzazione CD</span><span class="sxs-lookup"><span data-stu-id="9c198-298">CD Burning</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-299">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-299">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-300">%USERPROFILE%\Local locali\Dati Applicazioni\microsoft\masterizzazione CD Burning</span><span class="sxs-lookup"><span data-stu-id="9c198-300">%USERPROFILE%\Local Settings\Application Data\Microsoft\CD Burning</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ChangeRemovePrograms"></span><span id="folderid_changeremoveprograms"></span><span id="FOLDERID_CHANGEREMOVEPROGRAMS"></span><dl> <span data-ttu-id="9c198-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-302">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-302">GUID</span></span></td>
<td><span data-ttu-id="9c198-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span><span class="sxs-lookup"><span data-stu-id="9c198-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-304">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-304">Display Name</span></span></td>
<td><span data-ttu-id="9c198-305">Programmi e funzionalità</span><span class="sxs-lookup"><span data-stu-id="9c198-305">Programs and Features</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-306">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-306">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-307">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-307">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-308">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-308">Default Path</span></span></td>
<td><span data-ttu-id="9c198-309">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-309">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-310">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-310">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-311">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-311">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-312">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-312">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-313">Installazione applicazioni</span><span class="sxs-lookup"><span data-stu-id="9c198-313">Add or Remove Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-314">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-314">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-315">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-315">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonAdminTools"></span><span id="folderid_commonadmintools"></span><span id="FOLDERID_COMMONADMINTOOLS"></span><dl> <span data-ttu-id="9c198-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-317">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-317">GUID</span></span></td>
<td><span data-ttu-id="9c198-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span><span class="sxs-lookup"><span data-stu-id="9c198-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-319">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-319">Display Name</span></span></td>
<td><span data-ttu-id="9c198-320">Strumenti di amministrazione</span><span class="sxs-lookup"><span data-stu-id="9c198-320">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-321">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-321">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-322">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-322">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-323">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-323">Default Path</span></span></td>
<td><span data-ttu-id="9c198-324">Strumenti Avvio\Programmi\Strumenti%ALLUSERSPROFILE%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="9c198-324">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-325">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-325">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-326">CSIDL_COMMON_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="9c198-326">CSIDL_COMMON_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-327">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-327">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-328">Strumenti di amministrazione</span><span class="sxs-lookup"><span data-stu-id="9c198-328">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-329">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-329">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-330">Strumenti Avvio\Programmi\Strumenti%ALLUSERSPROFILE%\Menu</span><span class="sxs-lookup"><span data-stu-id="9c198-330">%ALLUSERSPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonOEMLinks"></span><span id="folderid_commonoemlinks"></span><span id="FOLDERID_COMMONOEMLINKS"></span><dl> <span data-ttu-id="9c198-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-332">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-332">GUID</span></span></td>
<td><span data-ttu-id="9c198-333">{C1BAE2D0-10DF-4334-BEDD-7AA20B227A9D}</span><span class="sxs-lookup"><span data-stu-id="9c198-333">{C1BAE2D0-10DF-4334-BEDD-7AA20B227A9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-334">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-334">Display Name</span></span></td>
<td><span data-ttu-id="9c198-335">Collegamenti OEM</span><span class="sxs-lookup"><span data-stu-id="9c198-335">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-336">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-336">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-337">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-337">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-338">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-338">Default Path</span></span></td>
<td><span data-ttu-id="9c198-339">Collegamenti%ALLUSERSPROFILE%\OEM</span><span class="sxs-lookup"><span data-stu-id="9c198-339">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-340">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-340">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-341">CSIDL_COMMON_OEM_LINKS</span><span class="sxs-lookup"><span data-stu-id="9c198-341">CSIDL_COMMON_OEM_LINKS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-342">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-342">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-343">Collegamenti OEM</span><span class="sxs-lookup"><span data-stu-id="9c198-343">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-344">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-344">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-345">Collegamenti%ALLUSERSPROFILE%\OEM</span><span class="sxs-lookup"><span data-stu-id="9c198-345">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonPrograms"></span><span id="folderid_commonprograms"></span><span id="FOLDERID_COMMONPROGRAMS"></span><dl> <span data-ttu-id="9c198-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-347">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-347">GUID</span></span></td>
<td><span data-ttu-id="9c198-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span><span class="sxs-lookup"><span data-stu-id="9c198-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-349">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-349">Display Name</span></span></td>
<td><span data-ttu-id="9c198-350">Programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-350">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-351">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-351">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-352">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-352">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-353">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-353">Default Path</span></span></td>
<td><span data-ttu-id="9c198-354">Avvio\programmi%ALLUSERSPROFILE%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="9c198-354">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-355">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-355">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-356">CSIDL_COMMON_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="9c198-356">CSIDL_COMMON_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-357">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-357">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-358">Programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-358">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-359">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-359">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-360">Avvio\programmi%ALLUSERSPROFILE%\Menu</span><span class="sxs-lookup"><span data-stu-id="9c198-360">%ALLUSERSPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonStartMenu"></span><span id="folderid_commonstartmenu"></span><span id="FOLDERID_COMMONSTARTMENU"></span><dl> <span data-ttu-id="9c198-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-362">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-362">GUID</span></span></td>
<td><span data-ttu-id="9c198-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span><span class="sxs-lookup"><span data-stu-id="9c198-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-364">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-364">Display Name</span></span></td>
<td><span data-ttu-id="9c198-365">Menu Start</span><span class="sxs-lookup"><span data-stu-id="9c198-365">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-366">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-366">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-367">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-367">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-368">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-368">Default Path</span></span></td>
<td><span data-ttu-id="9c198-369">Menu%ALLUSERSPROFILE%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="9c198-369">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-370">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-370">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-371">CSIDL_COMMON_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="9c198-371">CSIDL_COMMON_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-372">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-372">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-373">Menu Start</span><span class="sxs-lookup"><span data-stu-id="9c198-373">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-374">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-374">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-375">Menu%ALLUSERSPROFILE%\Menu</span><span class="sxs-lookup"><span data-stu-id="9c198-375">%ALLUSERSPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonStartup"></span><span id="folderid_commonstartup"></span><span id="FOLDERID_COMMONSTARTUP"></span><dl> <span data-ttu-id="9c198-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-377">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-377">GUID</span></span></td>
<td><span data-ttu-id="9c198-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span><span class="sxs-lookup"><span data-stu-id="9c198-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-379">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-379">Display Name</span></span></td>
<td><span data-ttu-id="9c198-380">Avvio</span><span class="sxs-lookup"><span data-stu-id="9c198-380">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-381">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-381">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-382">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-382">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-383">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-383">Default Path</span></span></td>
<td><span data-ttu-id="9c198-384">Avvio\programmi\esecuzione automatica%ALLUSERSPROFILE%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="9c198-384">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-385">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-385">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-386">CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="9c198-386">CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-387">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-387">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-388">Avvio</span><span class="sxs-lookup"><span data-stu-id="9c198-388">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-389">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-389">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-390">Avvio\programmi\esecuzione automatica%ALLUSERSPROFILE%\Menu</span><span class="sxs-lookup"><span data-stu-id="9c198-390">%ALLUSERSPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonTemplates"></span><span id="folderid_commontemplates"></span><span id="FOLDERID_COMMONTEMPLATES"></span><dl> <span data-ttu-id="9c198-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-392">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-392">GUID</span></span></td>
<td><span data-ttu-id="9c198-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span><span class="sxs-lookup"><span data-stu-id="9c198-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-394">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-394">Display Name</span></span></td>
<td><span data-ttu-id="9c198-395">Modelli</span><span class="sxs-lookup"><span data-stu-id="9c198-395">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-396">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-396">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-397">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-397">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-398">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-398">Default Path</span></span></td>
<td><span data-ttu-id="9c198-399">%ALLUSERSPROFILE%\Microsoft\Windows\Templates</span><span class="sxs-lookup"><span data-stu-id="9c198-399">%ALLUSERSPROFILE%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-400">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-400">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-401">CSIDL_COMMON_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="9c198-401">CSIDL_COMMON_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-402">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-402">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-403">Modelli</span><span class="sxs-lookup"><span data-stu-id="9c198-403">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-404">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-404">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-405">%ALLUSERSPROFILE%\Templates</span><span class="sxs-lookup"><span data-stu-id="9c198-405">%ALLUSERSPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ComputerFolder"></span><span id="folderid_computerfolder"></span><span id="FOLDERID_COMPUTERFOLDER"></span><dl> <span data-ttu-id="9c198-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-407">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-407">GUID</span></span></td>
<td><span data-ttu-id="9c198-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span><span class="sxs-lookup"><span data-stu-id="9c198-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-409">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-409">Display Name</span></span></td>
<td><span data-ttu-id="9c198-410">Computer</span><span class="sxs-lookup"><span data-stu-id="9c198-410">Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-411">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-411">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-412">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-412">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-413">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-413">Default Path</span></span></td>
<td><span data-ttu-id="9c198-414">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-414">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-415">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-415">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-416">CSIDL_DRIVES</span><span class="sxs-lookup"><span data-stu-id="9c198-416">CSIDL_DRIVES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-417">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-417">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-418">Risorse del computer</span><span class="sxs-lookup"><span data-stu-id="9c198-418">My Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-419">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-419">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-420">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-420">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ConflictFolder"></span><span id="folderid_conflictfolder"></span><span id="FOLDERID_CONFLICTFOLDER"></span><dl> <span data-ttu-id="9c198-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-422">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-422">GUID</span></span></td>
<td><span data-ttu-id="9c198-423">{4bfefb45-347d-4006-a5be-ac0cb0567192}</span><span class="sxs-lookup"><span data-stu-id="9c198-423">{4bfefb45-347d-4006-a5be-ac0cb0567192}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-424">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-424">Display Name</span></span></td>
<td><span data-ttu-id="9c198-425">Conflitti</span><span class="sxs-lookup"><span data-stu-id="9c198-425">Conflicts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-426">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-426">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-427">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-427">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-428">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-428">Default Path</span></span></td>
<td><span data-ttu-id="9c198-429">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-429">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-430">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-430">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-431">None, valore introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-431">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-432">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-432">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-433">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="9c198-433">Not applicable.</span></span> <span data-ttu-id="9c198-434">Questo <strong>KNOWNFOLDERID</strong> fa riferimento a Gestione sincronizzazione Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9c198-434">This <strong>KNOWNFOLDERID</strong> refers to the Windows Vista Synchronization Manager.</span></span> <span data-ttu-id="9c198-435">Non è la cartella a cui fa riferimento il <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a>precedente.</span><span class="sxs-lookup"><span data-stu-id="9c198-435">It is not the folder referenced by the older <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-436">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-436">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-437">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-437">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ConnectionsFolder"></span><span id="folderid_connectionsfolder"></span><span id="FOLDERID_CONNECTIONSFOLDER"></span><dl> <span data-ttu-id="9c198-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-439">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-439">GUID</span></span></td>
<td><span data-ttu-id="9c198-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span><span class="sxs-lookup"><span data-stu-id="9c198-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-441">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-441">Display Name</span></span></td>
<td><span data-ttu-id="9c198-442">Connessioni di rete</span><span class="sxs-lookup"><span data-stu-id="9c198-442">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-443">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-443">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-444">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-444">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-445">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-445">Default Path</span></span></td>
<td><span data-ttu-id="9c198-446">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-446">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-447">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-447">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-448">CSIDL_CONNECTIONS</span><span class="sxs-lookup"><span data-stu-id="9c198-448">CSIDL_CONNECTIONS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-449">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-449">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-450">Connessioni di rete</span><span class="sxs-lookup"><span data-stu-id="9c198-450">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-451">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-451">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-452">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-452">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Contacts"></span><span id="folderid_contacts"></span><span id="FOLDERID_CONTACTS"></span><dl> <span data-ttu-id="9c198-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-454">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-454">GUID</span></span></td>
<td><span data-ttu-id="9c198-455">{56784854-C6CB-462b-8169-88E350ACB882}</span><span class="sxs-lookup"><span data-stu-id="9c198-455">{56784854-C6CB-462b-8169-88E350ACB882}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-456">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-456">Display Name</span></span></td>
<td><span data-ttu-id="9c198-457">Contatti</span><span class="sxs-lookup"><span data-stu-id="9c198-457">Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-458">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-458">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-459">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-459">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-460">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-460">Default Path</span></span></td>
<td><span data-ttu-id="9c198-461">%USERPROFILE%\Contacts</span><span class="sxs-lookup"><span data-stu-id="9c198-461">%USERPROFILE%\Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-462">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-462">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-463">None, valore introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-463">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-464">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-464">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-465">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-465">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-466">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-466">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-467">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-467">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ControlPanelFolder"></span><span id="folderid_controlpanelfolder"></span><span id="FOLDERID_CONTROLPANELFOLDER"></span><dl> <span data-ttu-id="9c198-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-469">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-469">GUID</span></span></td>
<td><span data-ttu-id="9c198-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span><span class="sxs-lookup"><span data-stu-id="9c198-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-471">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-471">Display Name</span></span></td>
<td><span data-ttu-id="9c198-472">Control panel</span><span class="sxs-lookup"><span data-stu-id="9c198-472">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-473">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-473">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-474">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-474">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-475">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-475">Default Path</span></span></td>
<td><span data-ttu-id="9c198-476">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-476">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-477">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-477">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-478">CSIDL_CONTROLS</span><span class="sxs-lookup"><span data-stu-id="9c198-478">CSIDL_CONTROLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-479">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-479">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-480">Control panel</span><span class="sxs-lookup"><span data-stu-id="9c198-480">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-481">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-481">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-482">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-482">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Cookies"></span><span id="folderid_cookies"></span><span id="FOLDERID_COOKIES"></span><dl> <span data-ttu-id="9c198-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-484">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-484">GUID</span></span></td>
<td><span data-ttu-id="9c198-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span><span class="sxs-lookup"><span data-stu-id="9c198-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-486">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-486">Display Name</span></span></td>
<td><span data-ttu-id="9c198-487">Cookie</span><span class="sxs-lookup"><span data-stu-id="9c198-487">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-488">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-488">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-489">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-489">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-490">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-490">Default Path</span></span></td>
<td><span data-ttu-id="9c198-491">%APPDATA%\Microsoft\Windows\Cookies</span><span class="sxs-lookup"><span data-stu-id="9c198-491">%APPDATA%\Microsoft\Windows\Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-492">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-492">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-493">CSIDL_COOKIES</span><span class="sxs-lookup"><span data-stu-id="9c198-493">CSIDL_COOKIES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-494">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-494">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-495">Cookie</span><span class="sxs-lookup"><span data-stu-id="9c198-495">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-496">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-496">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-497">%USERPROFILE%\Cookies</span><span class="sxs-lookup"><span data-stu-id="9c198-497">%USERPROFILE%\Cookies</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Desktop"></span><span id="folderid_desktop"></span><span id="FOLDERID_DESKTOP"></span><dl> <span data-ttu-id="9c198-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-499">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-499">GUID</span></span></td>
<td><span data-ttu-id="9c198-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span><span class="sxs-lookup"><span data-stu-id="9c198-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-501">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-501">Display Name</span></span></td>
<td><span data-ttu-id="9c198-502">Desktop</span><span class="sxs-lookup"><span data-stu-id="9c198-502">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-503">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-503">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-504">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-504">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-505">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-505">Default Path</span></span></td>
<td><span data-ttu-id="9c198-506">%USERPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="9c198-506">%USERPROFILE%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-507">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-507">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-508">CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="9c198-508">CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-509">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-509">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-510">Desktop</span><span class="sxs-lookup"><span data-stu-id="9c198-510">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-511">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-511">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-512">%USERPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="9c198-512">%USERPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DeviceMetadataStore"></span><span id="folderid_devicemetadatastore"></span><span id="FOLDERID_DEVICEMETADATASTORE"></span><dl> <span data-ttu-id="9c198-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-514">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-514">GUID</span></span></td>
<td><span data-ttu-id="9c198-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span><span class="sxs-lookup"><span data-stu-id="9c198-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-516">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-516">Display Name</span></span></td>
<td><span data-ttu-id="9c198-517">DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="9c198-517">DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-518">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-518">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-519">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-519">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-520">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-520">Default Path</span></span></td>
<td><span data-ttu-id="9c198-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="9c198-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-522">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-522">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-523">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-523">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-524">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-524">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-525">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-525">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-526">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-526">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-527">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-527">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Documents"></span><span id="folderid_documents"></span><span id="FOLDERID_DOCUMENTS"></span><dl> <span data-ttu-id="9c198-528"><dt><strong>FOLDERID_Documents</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-528"><dt><strong>FOLDERID_Documents</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-529">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-529">GUID</span></span></td>
<td><span data-ttu-id="9c198-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span><span class="sxs-lookup"><span data-stu-id="9c198-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-531">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-531">Display Name</span></span></td>
<td><span data-ttu-id="9c198-532">Documenti</span><span class="sxs-lookup"><span data-stu-id="9c198-532">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-533">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-533">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-534">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-534">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-535">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-535">Default Path</span></span></td>
<td><span data-ttu-id="9c198-536">%UserProfile%\Documenti</span><span class="sxs-lookup"><span data-stu-id="9c198-536">%USERPROFILE%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-537">Equivalenti CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-537">CSIDL Equivalents</span></span></td>
<td><span data-ttu-id="9c198-538">CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="9c198-538">CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-539">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-539">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-540">Documenti</span><span class="sxs-lookup"><span data-stu-id="9c198-540">My Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-541">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-541">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-542">Documenti%USERPROFILE%\My</span><span class="sxs-lookup"><span data-stu-id="9c198-542">%USERPROFILE%\My Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DocumentsLibrary"></span><span id="folderid_documentslibrary"></span><span id="FOLDERID_DOCUMENTSLIBRARY"></span><dl> <span data-ttu-id="9c198-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-544">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-544">GUID</span></span></td>
<td><span data-ttu-id="9c198-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span><span class="sxs-lookup"><span data-stu-id="9c198-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-546">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-546">Display Name</span></span></td>
<td><span data-ttu-id="9c198-547">Documenti</span><span class="sxs-lookup"><span data-stu-id="9c198-547">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-548">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-548">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-549">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-549">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-550">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-550">Default Path</span></span></td>
<td><span data-ttu-id="9c198-551">%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</span><span class="sxs-lookup"><span data-stu-id="9c198-551">%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-552">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-552">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-553">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-553">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-554">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-554">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-555">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-555">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-556">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-556">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-557">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-557">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Downloads"></span><span id="folderid_downloads"></span><span id="FOLDERID_DOWNLOADS"></span><dl> <span data-ttu-id="9c198-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-559">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-559">GUID</span></span></td>
<td><span data-ttu-id="9c198-560">{374DE290-123F-4565-9164-39C4925E467B}</span><span class="sxs-lookup"><span data-stu-id="9c198-560">{374DE290-123F-4565-9164-39C4925E467B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-561">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-561">Display Name</span></span></td>
<td><span data-ttu-id="9c198-562">Download</span><span class="sxs-lookup"><span data-stu-id="9c198-562">Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-563">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-563">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-564">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-564">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-565">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-565">Default Path</span></span></td>
<td><span data-ttu-id="9c198-566">%USERPROFILE%\Downloads</span><span class="sxs-lookup"><span data-stu-id="9c198-566">%USERPROFILE%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-567">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-567">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-568">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-568">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-569">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-569">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-570">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-570">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-571">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-571">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-572">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-572">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Favorites"></span><span id="folderid_favorites"></span><span id="FOLDERID_FAVORITES"></span><dl> <span data-ttu-id="9c198-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-574">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-574">GUID</span></span></td>
<td><span data-ttu-id="9c198-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span><span class="sxs-lookup"><span data-stu-id="9c198-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-576">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-576">Display Name</span></span></td>
<td><span data-ttu-id="9c198-577">Preferiti</span><span class="sxs-lookup"><span data-stu-id="9c198-577">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-578">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-578">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-579">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-579">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-580">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-580">Default Path</span></span></td>
<td><span data-ttu-id="9c198-581">%USERPROFILE%\Favorites</span><span class="sxs-lookup"><span data-stu-id="9c198-581">%USERPROFILE%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-582">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-582">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-583">CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</span><span class="sxs-lookup"><span data-stu-id="9c198-583">CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-584">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-584">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-585">Preferiti</span><span class="sxs-lookup"><span data-stu-id="9c198-585">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-586">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-586">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-587">%USERPROFILE%\Favorites</span><span class="sxs-lookup"><span data-stu-id="9c198-587">%USERPROFILE%\Favorites</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Fonts"></span><span id="folderid_fonts"></span><span id="FOLDERID_FONTS"></span><dl> <span data-ttu-id="9c198-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-589">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-589">GUID</span></span></td>
<td><span data-ttu-id="9c198-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span><span class="sxs-lookup"><span data-stu-id="9c198-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-591">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-591">Display Name</span></span></td>
<td><span data-ttu-id="9c198-592">Tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="9c198-592">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-593">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-593">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-594">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-594">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-595">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-595">Default Path</span></span></td>
<td><span data-ttu-id="9c198-596">%windir%\Fonts</span><span class="sxs-lookup"><span data-stu-id="9c198-596">%windir%\Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-597">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-597">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-598">CSIDL_FONTS</span><span class="sxs-lookup"><span data-stu-id="9c198-598">CSIDL_FONTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-599">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-599">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-600">Tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="9c198-600">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-601">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-601">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-602">%windir%\Fonts</span><span class="sxs-lookup"><span data-stu-id="9c198-602">%windir%\Fonts</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Games"></span><span id="folderid_games"></span><span id="FOLDERID_GAMES"></span><dl> <span data-ttu-id="9c198-603"><dt><strong>FOLDERID_Games</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-603"><dt><strong>FOLDERID_Games</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="9c198-604">Questo FOLDERID è deprecato in Windows 10, versione 1803 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="9c198-604">This FOLDERID is deprecated in Windows 10, version 1803 and later versions.</span></span> <span data-ttu-id="9c198-605">In queste versioni restituisce <strong>0x80070057-E_INVALIDARG</strong>
</span><span class="sxs-lookup"><span data-stu-id="9c198-605">In these versions, it returns <strong>0x80070057 - E_INVALIDARG</strong>
</span></span></blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-606">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-606">GUID</span></span></td>
<td><span data-ttu-id="9c198-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span><span class="sxs-lookup"><span data-stu-id="9c198-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-608">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-608">Display Name</span></span></td>
<td><span data-ttu-id="9c198-609">Giochi</span><span class="sxs-lookup"><span data-stu-id="9c198-609">Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-610">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-610">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-611">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-611">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-612">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-612">Default Path</span></span></td>
<td><span data-ttu-id="9c198-613">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-613">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-614">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-614">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-615">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-615">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-616">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-616">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-617">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-617">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-618">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-618">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-619">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-619">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_GameTasks"></span><span id="folderid_gametasks"></span><span id="FOLDERID_GAMETASKS"></span><dl> <span data-ttu-id="9c198-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-621">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-621">GUID</span></span></td>
<td><span data-ttu-id="9c198-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span><span class="sxs-lookup"><span data-stu-id="9c198-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-623">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-623">Display Name</span></span></td>
<td><span data-ttu-id="9c198-624">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="9c198-624">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-625">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-625">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-626">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-626">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-627">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-627">Default Path</span></span></td>
<td><span data-ttu-id="9c198-628">%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</span><span class="sxs-lookup"><span data-stu-id="9c198-628">%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-629">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-629">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-630">None, valore introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-630">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-631">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-631">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-632">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-632">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-633">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-633">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-634">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-634">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_History"></span><span id="folderid_history"></span><span id="FOLDERID_HISTORY"></span><dl> <span data-ttu-id="9c198-635"><dt><strong>FOLDERID_History</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-635"><dt><strong>FOLDERID_History</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-636">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-636">GUID</span></span></td>
<td><span data-ttu-id="9c198-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span><span class="sxs-lookup"><span data-stu-id="9c198-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-638">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-638">Display Name</span></span></td>
<td><span data-ttu-id="9c198-639">Cronologia</span><span class="sxs-lookup"><span data-stu-id="9c198-639">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-640">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-640">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-641">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-641">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-642">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-642">Default Path</span></span></td>
<td><span data-ttu-id="9c198-643">%LOCALAPPDATA%\Microsoft\Windows\History</span><span class="sxs-lookup"><span data-stu-id="9c198-643">%LOCALAPPDATA%\Microsoft\Windows\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-644">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-644">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-645">CSIDL_HISTORY</span><span class="sxs-lookup"><span data-stu-id="9c198-645">CSIDL_HISTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-646">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-646">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-647">Cronologia</span><span class="sxs-lookup"><span data-stu-id="9c198-647">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-648">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-648">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-649">Locali\cronologia%USERPROFILE%\Local</span><span class="sxs-lookup"><span data-stu-id="9c198-649">%USERPROFILE%\Local Settings\History</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_HomeGroup"></span><span id="folderid_homegroup"></span><span id="FOLDERID_HOMEGROUP"></span><dl> <span data-ttu-id="9c198-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-651">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-651">GUID</span></span></td>
<td><span data-ttu-id="9c198-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span><span class="sxs-lookup"><span data-stu-id="9c198-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-653">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-653">Display Name</span></span></td>
<td><span data-ttu-id="9c198-654">Gruppo Home</span><span class="sxs-lookup"><span data-stu-id="9c198-654">Homegroup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-655">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-655">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-656">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-656">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-657">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-657">Default Path</span></span></td>
<td><span data-ttu-id="9c198-658">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-658">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-659">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-659">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-660">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-660">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-661">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-661">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-662">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-662">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-663">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-663">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-664">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-664">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_HomeGroupCurrentUser"></span><span id="folderid_homegroupcurrentuser"></span><span id="FOLDERID_HOMEGROUPCURRENTUSER"></span><dl> <span data-ttu-id="9c198-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-666">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-666">GUID</span></span></td>
<td><span data-ttu-id="9c198-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span><span class="sxs-lookup"><span data-stu-id="9c198-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-668">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-668">Display Name</span></span></td>
<td><span data-ttu-id="9c198-669">Nome utente dell'utente (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="9c198-669">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-670">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-670">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-671">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-671">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-672">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-672">Default Path</span></span></td>
<td><span data-ttu-id="9c198-673">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-673">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-674">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-674">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-675">None, valore introdotto in Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c198-675">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-676">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-676">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-677">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-677">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-678">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-678">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-679">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-679">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ImplicitAppShortcuts"></span><span id="folderid_implicitappshortcuts"></span><span id="FOLDERID_IMPLICITAPPSHORTCUTS"></span><dl> <span data-ttu-id="9c198-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-681">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-681">GUID</span></span></td>
<td><span data-ttu-id="9c198-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span><span class="sxs-lookup"><span data-stu-id="9c198-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-683">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-683">Display Name</span></span></td>
<td><span data-ttu-id="9c198-684">ImplicitAppShortcuts</span><span class="sxs-lookup"><span data-stu-id="9c198-684">ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-685">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-685">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-686">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-686">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-687">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-687">Default Path</span></span></td>
<td><span data-ttu-id="9c198-688">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts</span><span class="sxs-lookup"><span data-stu-id="9c198-688">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-689">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-689">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-690">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-690">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-691">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-691">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-692">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-692">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-693">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-693">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-694">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-694">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_InternetCache"></span><span id="folderid_internetcache"></span><span id="FOLDERID_INTERNETCACHE"></span><dl> <span data-ttu-id="9c198-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-696">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-696">GUID</span></span></td>
<td><span data-ttu-id="9c198-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span><span class="sxs-lookup"><span data-stu-id="9c198-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-698">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-698">Display Name</span></span></td>
<td><span data-ttu-id="9c198-699">File temporanei di Internet</span><span class="sxs-lookup"><span data-stu-id="9c198-699">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-700">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-700">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-701">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-701">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-702">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-702">Default Path</span></span></td>
<td><span data-ttu-id="9c198-703">File%LOCALAPPDATA%\Microsoft\Windows\Temporary Internet</span><span class="sxs-lookup"><span data-stu-id="9c198-703">%LOCALAPPDATA%\Microsoft\Windows\Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-704">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-704">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-705">CSIDL_INTERNET_CACHE</span><span class="sxs-lookup"><span data-stu-id="9c198-705">CSIDL_INTERNET_CACHE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-706">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-706">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-707">File temporanei di Internet</span><span class="sxs-lookup"><span data-stu-id="9c198-707">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-708">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-708">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-709">File%USERPROFILE%\Local Locali\temporary Internet</span><span class="sxs-lookup"><span data-stu-id="9c198-709">%USERPROFILE%\Local Settings\Temporary Internet Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_InternetFolder"></span><span id="folderid_internetfolder"></span><span id="FOLDERID_INTERNETFOLDER"></span><dl> <span data-ttu-id="9c198-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-711">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-711">GUID</span></span></td>
<td><span data-ttu-id="9c198-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span><span class="sxs-lookup"><span data-stu-id="9c198-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-713">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-713">Display Name</span></span></td>
<td><span data-ttu-id="9c198-714">Internet</span><span class="sxs-lookup"><span data-stu-id="9c198-714">The Internet</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-715">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-715">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-716">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-716">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-717">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-717">Default Path</span></span></td>
<td><span data-ttu-id="9c198-718">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-718">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-719">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-719">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-720">CSIDL_INTERNET</span><span class="sxs-lookup"><span data-stu-id="9c198-720">CSIDL_INTERNET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-721">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-721">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-722">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="9c198-722">Internet Explorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-723">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-723">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-724">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-724">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Libraries"></span><span id="folderid_libraries"></span><span id="FOLDERID_LIBRARIES"></span><dl> <span data-ttu-id="9c198-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-726">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-726">GUID</span></span></td>
<td><span data-ttu-id="9c198-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span><span class="sxs-lookup"><span data-stu-id="9c198-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-728">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-728">Display Name</span></span></td>
<td><span data-ttu-id="9c198-729">Librerie</span><span class="sxs-lookup"><span data-stu-id="9c198-729">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-730">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-730">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-731">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-731">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-732">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-732">Default Path</span></span></td>
<td><span data-ttu-id="9c198-733">%APPDATA%\Microsoft\Windows\Libraries</span><span class="sxs-lookup"><span data-stu-id="9c198-733">%APPDATA%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-734">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-734">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-735">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-735">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-736">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-736">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-737">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-737">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-738">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-738">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-739">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-739">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Links"></span><span id="folderid_links"></span><span id="FOLDERID_LINKS"></span><dl> <span data-ttu-id="9c198-740"><dt><strong>FOLDERID_Links</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-740"><dt><strong>FOLDERID_Links</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-741">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-741">GUID</span></span></td>
<td><span data-ttu-id="9c198-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span><span class="sxs-lookup"><span data-stu-id="9c198-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-743">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-743">Display Name</span></span></td>
<td><span data-ttu-id="9c198-744">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="9c198-744">Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-745">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-745">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-746">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-746">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-747">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-747">Default Path</span></span></td>
<td><span data-ttu-id="9c198-748">%USERPROFILE%\Links</span><span class="sxs-lookup"><span data-stu-id="9c198-748">%USERPROFILE%\Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-749">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-749">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-750">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-750">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-751">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-751">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-752">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-752">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-753">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-753">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-754">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-754">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalAppData"></span><span id="folderid_localappdata"></span><span id="FOLDERID_LOCALAPPDATA"></span><dl> <span data-ttu-id="9c198-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-756">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-756">GUID</span></span></td>
<td><span data-ttu-id="9c198-757">F1B32785-6FBA-4FCF-9D55-7B8E7F157091</span><span class="sxs-lookup"><span data-stu-id="9c198-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-758">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-758">Display Name</span></span></td>
<td><span data-ttu-id="9c198-759">Locale</span><span class="sxs-lookup"><span data-stu-id="9c198-759">Local</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-760">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-760">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-761">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-761">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-762">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-762">Default Path</span></span></td>
<td><span data-ttu-id="9c198-763">% LOCALAPPDATA% (%USERPROFILE%\AppData\Local)</span><span class="sxs-lookup"><span data-stu-id="9c198-763">%LOCALAPPDATA% (%USERPROFILE%\AppData\Local)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-764">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-764">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-765">CSIDL_LOCAL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="9c198-765">CSIDL_LOCAL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-766">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-766">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-767">Dati applicazione</span><span class="sxs-lookup"><span data-stu-id="9c198-767">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-768">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-768">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-769">Dati locali\Dati%USERPROFILE%\Local</span><span class="sxs-lookup"><span data-stu-id="9c198-769">%USERPROFILE%\Local Settings\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_LocalAppDataLow"></span><span id="folderid_localappdatalow"></span><span id="FOLDERID_LOCALAPPDATALOW"></span><dl> <span data-ttu-id="9c198-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-771">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-771">GUID</span></span></td>
<td><span data-ttu-id="9c198-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span><span class="sxs-lookup"><span data-stu-id="9c198-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-773">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-773">Display Name</span></span></td>
<td><span data-ttu-id="9c198-774">LocalLow</span><span class="sxs-lookup"><span data-stu-id="9c198-774">LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-775">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-775">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-776">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-776">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-777">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-777">Default Path</span></span></td>
<td><span data-ttu-id="9c198-778">%USERPROFILE%\AppData\LocalLow</span><span class="sxs-lookup"><span data-stu-id="9c198-778">%USERPROFILE%\AppData\LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-779">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-779">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-780">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-780">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-781">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-781">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-782">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-782">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-783">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-783">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-784">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-784">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalizedResourcesDir"></span><span id="folderid_localizedresourcesdir"></span><span id="FOLDERID_LOCALIZEDRESOURCESDIR"></span><dl> <span data-ttu-id="9c198-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-786">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-786">GUID</span></span></td>
<td><span data-ttu-id="9c198-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span><span class="sxs-lookup"><span data-stu-id="9c198-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-788">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-788">Display Name</span></span></td>
<td><span data-ttu-id="9c198-789">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-789">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-790">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-790">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-791">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-791">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-792">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-792">Default Path</span></span></td>
<td><span data-ttu-id="9c198-793">%WINDIR%\resources\0409 (tabella codici)</span><span class="sxs-lookup"><span data-stu-id="9c198-793">%windir%\resources\0409 (code page)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-794">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-794">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-795">CSIDL_RESOURCES_LOCALIZED</span><span class="sxs-lookup"><span data-stu-id="9c198-795">CSIDL_RESOURCES_LOCALIZED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-796">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-796">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-797">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-797">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-798">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-798">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-799">%WINDIR%\resources\0409 (tabella codici)</span><span class="sxs-lookup"><span data-stu-id="9c198-799">%windir%\resources\0409 (code page)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Music"></span><span id="folderid_music"></span><span id="FOLDERID_MUSIC"></span><dl> <span data-ttu-id="9c198-800"><dt><strong>FOLDERID_Music</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-800"><dt><strong>FOLDERID_Music</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-801">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-801">GUID</span></span></td>
<td><span data-ttu-id="9c198-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span><span class="sxs-lookup"><span data-stu-id="9c198-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-803">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-803">Display Name</span></span></td>
<td><span data-ttu-id="9c198-804">Musica</span><span class="sxs-lookup"><span data-stu-id="9c198-804">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-805">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-805">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-806">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-806">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-807">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-807">Default Path</span></span></td>
<td><span data-ttu-id="9c198-808">%USERPROFILE%\Music</span><span class="sxs-lookup"><span data-stu-id="9c198-808">%USERPROFILE%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-809">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-809">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-810">CSIDL_MYMUSIC</span><span class="sxs-lookup"><span data-stu-id="9c198-810">CSIDL_MYMUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-811">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-811">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-812">Musica</span><span class="sxs-lookup"><span data-stu-id="9c198-812">My Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-813">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-813">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-814">%USERPROFILE%\My di musica</span><span class="sxs-lookup"><span data-stu-id="9c198-814">%USERPROFILE%\My Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_MusicLibrary"></span><span id="folderid_musiclibrary"></span><span id="FOLDERID_MUSICLIBRARY"></span><dl> <span data-ttu-id="9c198-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-816">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-816">GUID</span></span></td>
<td><span data-ttu-id="9c198-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span><span class="sxs-lookup"><span data-stu-id="9c198-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-818">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-818">Display Name</span></span></td>
<td><span data-ttu-id="9c198-819">Musica</span><span class="sxs-lookup"><span data-stu-id="9c198-819">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-820">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-820">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-821">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-821">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-822">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-822">Default Path</span></span></td>
<td><span data-ttu-id="9c198-823">%APPDATA%\Microsoft\Windows\Libraries\Music.library-ms</span><span class="sxs-lookup"><span data-stu-id="9c198-823">%APPDATA%\Microsoft\Windows\Libraries\Music.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-824">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-824">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-825">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-825">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-826">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-826">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-827">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-827">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-828">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-828">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-829">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-829">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_NetHood"></span><span id="folderid_nethood"></span><span id="FOLDERID_NETHOOD"></span><dl> <span data-ttu-id="9c198-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-831">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-831">GUID</span></span></td>
<td><span data-ttu-id="9c198-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span><span class="sxs-lookup"><span data-stu-id="9c198-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-833">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-833">Display Name</span></span></td>
<td><span data-ttu-id="9c198-834">Collegamenti di rete</span><span class="sxs-lookup"><span data-stu-id="9c198-834">Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-835">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-835">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-836">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-836">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-837">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-837">Default Path</span></span></td>
<td><span data-ttu-id="9c198-838">Collegamenti%APPDATA%\Microsoft\Windows\Network</span><span class="sxs-lookup"><span data-stu-id="9c198-838">%APPDATA%\Microsoft\Windows\Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-839">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-839">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-840">CSIDL_NETHOOD</span><span class="sxs-lookup"><span data-stu-id="9c198-840">CSIDL_NETHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-841">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-841">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-842">NetHood</span><span class="sxs-lookup"><span data-stu-id="9c198-842">NetHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-843">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-843">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-844">%USERPROFILE%\NetHood</span><span class="sxs-lookup"><span data-stu-id="9c198-844">%USERPROFILE%\NetHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_NetworkFolder"></span><span id="folderid_networkfolder"></span><span id="FOLDERID_NETWORKFOLDER"></span><dl> <span data-ttu-id="9c198-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-846">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-846">GUID</span></span></td>
<td><span data-ttu-id="9c198-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span><span class="sxs-lookup"><span data-stu-id="9c198-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-848">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-848">Display Name</span></span></td>
<td><span data-ttu-id="9c198-849">Rete</span><span class="sxs-lookup"><span data-stu-id="9c198-849">Network</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-850">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-850">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-851">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-851">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-852">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-852">Default Path</span></span></td>
<td><span data-ttu-id="9c198-853">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-853">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-854">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-854">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-855">CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</span><span class="sxs-lookup"><span data-stu-id="9c198-855">CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-856">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-856">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-857">Risorse di rete</span><span class="sxs-lookup"><span data-stu-id="9c198-857">My Network Places</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-858">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-858">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-859">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-859">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Objects3D"></span><span id="folderid_objects3d"></span><span id="FOLDERID_OBJECTS3D"></span><dl> <span data-ttu-id="9c198-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-861">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-861">GUID</span></span></td>
<td><span data-ttu-id="9c198-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span><span class="sxs-lookup"><span data-stu-id="9c198-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-863">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-863">Display Name</span></span></td>
<td><span data-ttu-id="9c198-864">Oggetti 3D</span><span class="sxs-lookup"><span data-stu-id="9c198-864">3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-865">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-865">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-866">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-866">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-867">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-867">Default Path</span></span></td>
<td><span data-ttu-id="9c198-868">Oggetti%USERPROFILE%\3D</span><span class="sxs-lookup"><span data-stu-id="9c198-868">%USERPROFILE%\3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-869">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-869">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-870">None, valore introdotto in Windows 10, versione 1703</span><span class="sxs-lookup"><span data-stu-id="9c198-870">None, value introduced in Windows 10, version 1703</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-871">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-871">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-872">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-872">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-873">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-873">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-874">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-874">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_OriginalImages"></span><span id="folderid_originalimages"></span><span id="FOLDERID_ORIGINALIMAGES"></span><dl> <span data-ttu-id="9c198-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-876">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-876">GUID</span></span></td>
<td><span data-ttu-id="9c198-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span><span class="sxs-lookup"><span data-stu-id="9c198-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-878">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-878">Display Name</span></span></td>
<td><span data-ttu-id="9c198-879">Immagini originali</span><span class="sxs-lookup"><span data-stu-id="9c198-879">Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-880">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-880">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-881">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-881">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-882">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-882">Default Path</span></span></td>
<td><span data-ttu-id="9c198-883">Immagini di Gallery\Original foto%LOCALAPPDATA%\Microsoft\Windows</span><span class="sxs-lookup"><span data-stu-id="9c198-883">%LOCALAPPDATA%\Microsoft\Windows Photo Gallery\Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-884">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-884">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-885">None, valore introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-885">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-886">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-886">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-887">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-887">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-888">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-888">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-889">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-889">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PhotoAlbums"></span><span id="folderid_photoalbums"></span><span id="FOLDERID_PHOTOALBUMS"></span><dl> <span data-ttu-id="9c198-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-891">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-891">GUID</span></span></td>
<td><span data-ttu-id="9c198-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span><span class="sxs-lookup"><span data-stu-id="9c198-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-893">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-893">Display Name</span></span></td>
<td><span data-ttu-id="9c198-894">Presentazioni</span><span class="sxs-lookup"><span data-stu-id="9c198-894">Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-895">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-895">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-896">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-896">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-897">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-897">Default Path</span></span></td>
<td><span data-ttu-id="9c198-898">%USERPROFILE%\Pictures\Slide Mostra</span><span class="sxs-lookup"><span data-stu-id="9c198-898">%USERPROFILE%\Pictures\Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-899">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-899">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-900">None, valore introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-900">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-901">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-901">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-902">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-902">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-903">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-903">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-904">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-904">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PicturesLibrary"></span><span id="folderid_pictureslibrary"></span><span id="FOLDERID_PICTURESLIBRARY"></span><dl> <span data-ttu-id="9c198-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-906">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-906">GUID</span></span></td>
<td><span data-ttu-id="9c198-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span><span class="sxs-lookup"><span data-stu-id="9c198-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-908">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-908">Display Name</span></span></td>
<td><span data-ttu-id="9c198-909">Immagini</span><span class="sxs-lookup"><span data-stu-id="9c198-909">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-910">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-910">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-911">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-911">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-912">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-912">Default Path</span></span></td>
<td><span data-ttu-id="9c198-913">%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</span><span class="sxs-lookup"><span data-stu-id="9c198-913">%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-914">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-914">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-915">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-915">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-916">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-916">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-917">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-917">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-918">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-918">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-919">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-919">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Pictures"></span><span id="folderid_pictures"></span><span id="FOLDERID_PICTURES"></span><dl> <span data-ttu-id="9c198-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-921">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-921">GUID</span></span></td>
<td><span data-ttu-id="9c198-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span><span class="sxs-lookup"><span data-stu-id="9c198-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-923">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-923">Display Name</span></span></td>
<td><span data-ttu-id="9c198-924">Immagini</span><span class="sxs-lookup"><span data-stu-id="9c198-924">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-925">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-925">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-926">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-926">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-927">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-927">Default Path</span></span></td>
<td><span data-ttu-id="9c198-928">%USERPROFILE%\Pictures</span><span class="sxs-lookup"><span data-stu-id="9c198-928">%USERPROFILE%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-929">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-929">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-930">CSIDL_MYPICTURES</span><span class="sxs-lookup"><span data-stu-id="9c198-930">CSIDL_MYPICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-931">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-931">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-932">Immagini personali</span><span class="sxs-lookup"><span data-stu-id="9c198-932">My Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-933">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-933">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-934">Immagini di%USERPROFILE%\My</span><span class="sxs-lookup"><span data-stu-id="9c198-934">%USERPROFILE%\My Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Playlists"></span><span id="folderid_playlists"></span><span id="FOLDERID_PLAYLISTS"></span><dl> <span data-ttu-id="9c198-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-936">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-936">GUID</span></span></td>
<td><span data-ttu-id="9c198-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span><span class="sxs-lookup"><span data-stu-id="9c198-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-938">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-938">Display Name</span></span></td>
<td><span data-ttu-id="9c198-939">Playlist</span><span class="sxs-lookup"><span data-stu-id="9c198-939">Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-940">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-940">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-941">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-941">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-942">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-942">Default Path</span></span></td>
<td><span data-ttu-id="9c198-943">%USERPROFILE%\Music\Playlists</span><span class="sxs-lookup"><span data-stu-id="9c198-943">%USERPROFILE%\Music\Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-944">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-944">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-945">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-945">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-946">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-946">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-947">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-947">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-948">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-948">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-949">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-949">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PrintersFolder"></span><span id="folderid_printersfolder"></span><span id="FOLDERID_PRINTERSFOLDER"></span><dl> <span data-ttu-id="9c198-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-951">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-951">GUID</span></span></td>
<td><span data-ttu-id="9c198-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span><span class="sxs-lookup"><span data-stu-id="9c198-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-953">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-953">Display Name</span></span></td>
<td><span data-ttu-id="9c198-954">Stampanti</span><span class="sxs-lookup"><span data-stu-id="9c198-954">Printers</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-955">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-955">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-956">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-956">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-957">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-957">Default Path</span></span></td>
<td><span data-ttu-id="9c198-958">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-958">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-959">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-959">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-960">CSIDL_PRINTERS</span><span class="sxs-lookup"><span data-stu-id="9c198-960">CSIDL_PRINTERS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-961">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-961">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-962">Stampanti e fax</span><span class="sxs-lookup"><span data-stu-id="9c198-962">Printers and Faxes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-963">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-963">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-964">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-964">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PrintHood"></span><span id="folderid_printhood"></span><span id="FOLDERID_PRINTHOOD"></span><dl> <span data-ttu-id="9c198-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-966">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-966">GUID</span></span></td>
<td><span data-ttu-id="9c198-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span><span class="sxs-lookup"><span data-stu-id="9c198-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-968">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-968">Display Name</span></span></td>
<td><span data-ttu-id="9c198-969">Collegamenti stampanti</span><span class="sxs-lookup"><span data-stu-id="9c198-969">Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-970">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-970">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-971">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-971">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-972">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-972">Default Path</span></span></td>
<td><span data-ttu-id="9c198-973">Collegamenti%APPDATA%\Microsoft\Windows\Printer</span><span class="sxs-lookup"><span data-stu-id="9c198-973">%APPDATA%\Microsoft\Windows\Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-974">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-974">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-975">CSIDL_PRINTHOOD</span><span class="sxs-lookup"><span data-stu-id="9c198-975">CSIDL_PRINTHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-976">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-976">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-977">PrintHood</span><span class="sxs-lookup"><span data-stu-id="9c198-977">PrintHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-978">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-978">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-979">%USERPROFILE%\PrintHood</span><span class="sxs-lookup"><span data-stu-id="9c198-979">%USERPROFILE%\PrintHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Profile"></span><span id="folderid_profile"></span><span id="FOLDERID_PROFILE"></span><dl> <span data-ttu-id="9c198-980"><dt><strong>FOLDERID_Profile</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-980"><dt><strong>FOLDERID_Profile</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-981">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-981">GUID</span></span></td>
<td><span data-ttu-id="9c198-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span><span class="sxs-lookup"><span data-stu-id="9c198-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-983">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-983">Display Name</span></span></td>
<td><span data-ttu-id="9c198-984">Nome utente dell'utente (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="9c198-984">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-985">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-985">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-986">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-986">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-987">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-987">Default Path</span></span></td>
<td><span data-ttu-id="9c198-988">% USERPROFILE% (%SystemDrive%\Users \% nomeutente%)</span><span class="sxs-lookup"><span data-stu-id="9c198-988">%USERPROFILE% (%SystemDrive%\Users\%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-989">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-989">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-990">CSIDL_PROFILE</span><span class="sxs-lookup"><span data-stu-id="9c198-990">CSIDL_PROFILE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-991">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-991">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-992">Nome utente dell'utente (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="9c198-992">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-993">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-993">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-994">% USERPROFILE% (%SystemDrive%\Documents e impostazioni \% nome utente%)</span><span class="sxs-lookup"><span data-stu-id="9c198-994">%USERPROFILE% (%SystemDrive%\Documents and Settings\%USERNAME%)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramData"></span><span id="folderid_programdata"></span><span id="FOLDERID_PROGRAMDATA"></span><dl> <span data-ttu-id="9c198-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-996">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-996">GUID</span></span></td>
<td><span data-ttu-id="9c198-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span><span class="sxs-lookup"><span data-stu-id="9c198-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-998">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-998">Display Name</span></span></td>
<td><span data-ttu-id="9c198-999">ProgramData</span><span class="sxs-lookup"><span data-stu-id="9c198-999">ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1000">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1000">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1001">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1001">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1002">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1002">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1003">% ALLUSERSPROFILE% (% ProgramData%,%SystemDrive%\ProgramData)</span><span class="sxs-lookup"><span data-stu-id="9c198-1003">%ALLUSERSPROFILE% (%ProgramData%, %SystemDrive%\ProgramData)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1004">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1004">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1005">CSIDL_COMMON_APPDATA</span><span class="sxs-lookup"><span data-stu-id="9c198-1005">CSIDL_COMMON_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1006">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1006">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1007">Dati applicazione</span><span class="sxs-lookup"><span data-stu-id="9c198-1007">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1008">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1008">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1009">Dati%ALLUSERSPROFILE%\Application</span><span class="sxs-lookup"><span data-stu-id="9c198-1009">%ALLUSERSPROFILE%\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFiles"></span><span id="folderid_programfiles"></span><span id="FOLDERID_PROGRAMFILES"></span><dl> <span data-ttu-id="9c198-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9c198-1011">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="9c198-1011">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1012">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1012">GUID</span></span></td>
<td><span data-ttu-id="9c198-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span><span class="sxs-lookup"><span data-stu-id="9c198-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1014">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1014">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1015">Programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-1015">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1016">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1016">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1017">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1017">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1018">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1018">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1019">% Programmi% (file%SystemDrive%\Program)</span><span class="sxs-lookup"><span data-stu-id="9c198-1019">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1020">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1020">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1021">CSIDL_PROGRAM_FILES</span><span class="sxs-lookup"><span data-stu-id="9c198-1021">CSIDL_PROGRAM_FILES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1022">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1022">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1023">Programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-1023">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1024">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1024">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1025">% Programmi% (file%SystemDrive%\Program)</span><span class="sxs-lookup"><span data-stu-id="9c198-1025">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX64"></span><span id="folderid_programfilesx64"></span><span id="FOLDERID_PROGRAMFILESX64"></span><dl> <span data-ttu-id="9c198-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9c198-1027">Questo valore non è supportato nei sistemi operativi a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9c198-1027">This value is not supported on 32-bit operating systems.</span></span> <span data-ttu-id="9c198-1028">Non è inoltre supportata per le applicazioni a 32 bit in esecuzione su sistemi operativi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9c198-1028">It also is not supported for 32-bit applications running on 64-bit operating systems.</span></span> <span data-ttu-id="9c198-1029">Il tentativo di utilizzare FOLDERID_ProgramFilesX64 in una delle due situazioni genera un errore.</span><span class="sxs-lookup"><span data-stu-id="9c198-1029">Attempting to use FOLDERID_ProgramFilesX64 in either situation results in an error.</span></span> <span data-ttu-id="9c198-1030">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="9c198-1030">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1031">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1031">GUID</span></span></td>
<td><span data-ttu-id="9c198-1032">{6D809377-6AF0-444B-8957-A3773F02200E}</span><span class="sxs-lookup"><span data-stu-id="9c198-1032">{6D809377-6AF0-444b-8957-A3773F02200E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1033">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1033">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1034">Programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-1034">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1035">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1035">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1036">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1036">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1037">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1037">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1038">% Programmi% (file%SystemDrive%\Program)</span><span class="sxs-lookup"><span data-stu-id="9c198-1038">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1039">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1039">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1040">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1040">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1041">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1041">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1042">Programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-1042">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1043">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1043">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1044">% Programmi% (file%SystemDrive%\Program)</span><span class="sxs-lookup"><span data-stu-id="9c198-1044">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX86"></span><span id="folderid_programfilesx86"></span><span id="FOLDERID_PROGRAMFILESX86"></span><dl> <span data-ttu-id="9c198-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9c198-1046">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="9c198-1046">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1047">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1047">GUID</span></span></td>
<td><span data-ttu-id="9c198-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span><span class="sxs-lookup"><span data-stu-id="9c198-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1049">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1049">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1050">Programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-1050">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1051">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1051">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1052">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1052">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1053">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1053">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1054">% Programmi% (file%SystemDrive%\Program)</span><span class="sxs-lookup"><span data-stu-id="9c198-1054">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1055">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1055">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1056">CSIDL_PROGRAM_FILESX86</span><span class="sxs-lookup"><span data-stu-id="9c198-1056">CSIDL_PROGRAM_FILESX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1057">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1057">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1058">Programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-1058">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1059">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1059">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1060">% Programmi% (file%SystemDrive%\Program)</span><span class="sxs-lookup"><span data-stu-id="9c198-1060">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommon"></span><span id="folderid_programfilescommon"></span><span id="FOLDERID_PROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="9c198-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9c198-1062">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="9c198-1062">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1063">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1063">GUID</span></span></td>
<td><span data-ttu-id="9c198-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span><span class="sxs-lookup"><span data-stu-id="9c198-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1065">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1065">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1066">File comuni</span><span class="sxs-lookup"><span data-stu-id="9c198-1066">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1067">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1067">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1068">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1068">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1069">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1069">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1070">File%programmi%\Common</span><span class="sxs-lookup"><span data-stu-id="9c198-1070">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1071">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1071">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1072">CSIDL_PROGRAM_FILES_COMMON</span><span class="sxs-lookup"><span data-stu-id="9c198-1072">CSIDL_PROGRAM_FILES_COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1073">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1073">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1074">File comuni</span><span class="sxs-lookup"><span data-stu-id="9c198-1074">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1075">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1075">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1076">File%programmi%\Common</span><span class="sxs-lookup"><span data-stu-id="9c198-1076">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX64"></span><span id="folderid_programfilescommonx64"></span><span id="FOLDERID_PROGRAMFILESCOMMONX64"></span><dl> <span data-ttu-id="9c198-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9c198-1078">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="9c198-1078">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1079">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1079">GUID</span></span></td>
<td><span data-ttu-id="9c198-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span><span class="sxs-lookup"><span data-stu-id="9c198-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1081">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1081">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1082">File comuni</span><span class="sxs-lookup"><span data-stu-id="9c198-1082">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1083">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1083">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1084">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1084">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1085">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1085">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1086">File%programmi%\Common</span><span class="sxs-lookup"><span data-stu-id="9c198-1086">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1087">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1087">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1088">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1088">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1089">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1089">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1090">File comuni</span><span class="sxs-lookup"><span data-stu-id="9c198-1090">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1091">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1091">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1092">File%programmi%\Common</span><span class="sxs-lookup"><span data-stu-id="9c198-1092">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX86"></span><span id="folderid_programfilescommonx86"></span><span id="FOLDERID_PROGRAMFILESCOMMONX86"></span><dl> <span data-ttu-id="9c198-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9c198-1094">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="9c198-1094">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1095">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1095">GUID</span></span></td>
<td><span data-ttu-id="9c198-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span><span class="sxs-lookup"><span data-stu-id="9c198-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1097">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1097">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1098">File comuni</span><span class="sxs-lookup"><span data-stu-id="9c198-1098">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1099">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1099">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1100">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1100">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1101">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1101">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1102">File%programmi%\Common</span><span class="sxs-lookup"><span data-stu-id="9c198-1102">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1103">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1103">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1104">CSIDL_PROGRAM_FILES_COMMONX86</span><span class="sxs-lookup"><span data-stu-id="9c198-1104">CSIDL_PROGRAM_FILES_COMMONX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1105">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1105">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1106">File comuni</span><span class="sxs-lookup"><span data-stu-id="9c198-1106">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1107">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1107">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1108">File%programmi%\Common</span><span class="sxs-lookup"><span data-stu-id="9c198-1108">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Programs"></span><span id="folderid_programs"></span><span id="FOLDERID_PROGRAMS"></span><dl> <span data-ttu-id="9c198-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1110">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1110">GUID</span></span></td>
<td><span data-ttu-id="9c198-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span><span class="sxs-lookup"><span data-stu-id="9c198-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1112">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1112">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1113">Programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-1113">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1114">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1114">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1115">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1115">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1116">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1116">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1117">Avvio\programmi%APPDATA%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="9c198-1117">%APPDATA%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1118">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1118">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1119">CSIDL_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="9c198-1119">CSIDL_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1120">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1120">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1121">Programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-1121">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1122">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1122">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1123">Avvio\programmi%USERPROFILE%\Menu</span><span class="sxs-lookup"><span data-stu-id="9c198-1123">%USERPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Public"></span><span id="folderid_public"></span><span id="FOLDERID_PUBLIC"></span><dl> <span data-ttu-id="9c198-1124"><dt><strong>FOLDERID_Public</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1124"><dt><strong>FOLDERID_Public</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1125">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1125">GUID</span></span></td>
<td><span data-ttu-id="9c198-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span><span class="sxs-lookup"><span data-stu-id="9c198-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1127">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1127">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1128">Pubblico</span><span class="sxs-lookup"><span data-stu-id="9c198-1128">Public</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1129">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1129">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1130">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1130">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1131">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1131">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1132">% PUBLIC% (%SystemDrive%\Users\Public)</span><span class="sxs-lookup"><span data-stu-id="9c198-1132">%PUBLIC% (%SystemDrive%\Users\Public)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1133">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1133">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1134">Nessuno, nuovo per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-1134">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1135">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1135">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1136">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1136">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1137">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1137">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1138">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1138">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDesktop"></span><span id="folderid_publicdesktop"></span><span id="FOLDERID_PUBLICDESKTOP"></span><dl> <span data-ttu-id="9c198-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1140">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1140">GUID</span></span></td>
<td><span data-ttu-id="9c198-1141">{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</span><span class="sxs-lookup"><span data-stu-id="9c198-1141">{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1142">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1142">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1143">Desktop pubblico</span><span class="sxs-lookup"><span data-stu-id="9c198-1143">Public Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1144">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1144">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1145">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1145">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1146">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1146">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1147">%PUBLIC%\Desktop</span><span class="sxs-lookup"><span data-stu-id="9c198-1147">%PUBLIC%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1148">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1148">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="9c198-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1150">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1150">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1151">Desktop</span><span class="sxs-lookup"><span data-stu-id="9c198-1151">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1152">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1152">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1153">%ALLUSERSPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="9c198-1153">%ALLUSERSPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicDocuments"></span><span id="folderid_publicdocuments"></span><span id="FOLDERID_PUBLICDOCUMENTS"></span><dl> <span data-ttu-id="9c198-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1155">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1155">GUID</span></span></td>
<td><span data-ttu-id="9c198-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span><span class="sxs-lookup"><span data-stu-id="9c198-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1157">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1157">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1158">Documenti pubblici</span><span class="sxs-lookup"><span data-stu-id="9c198-1158">Public Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1159">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1159">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1160">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1160">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1161">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1161">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1162">%PUBLIC%\Documents</span><span class="sxs-lookup"><span data-stu-id="9c198-1162">%PUBLIC%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1163">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1163">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1164">CSIDL_COMMON_DOCUMENTS</span><span class="sxs-lookup"><span data-stu-id="9c198-1164">CSIDL_COMMON_DOCUMENTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1165">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1165">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1166">Documenti condivisi</span><span class="sxs-lookup"><span data-stu-id="9c198-1166">Shared Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1167">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1167">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1168">%ALLUSERSPROFILE%\Documents</span><span class="sxs-lookup"><span data-stu-id="9c198-1168">%ALLUSERSPROFILE%\Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDownloads"></span><span id="folderid_publicdownloads"></span><span id="FOLDERID_PUBLICDOWNLOADS"></span><dl> <span data-ttu-id="9c198-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1170">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1170">GUID</span></span></td>
<td><span data-ttu-id="9c198-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span><span class="sxs-lookup"><span data-stu-id="9c198-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1172">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1172">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1173">Download pubblici</span><span class="sxs-lookup"><span data-stu-id="9c198-1173">Public Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1174">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1174">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1175">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1175">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1176">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1176">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1177">%PUBLIC%\Downloads</span><span class="sxs-lookup"><span data-stu-id="9c198-1177">%PUBLIC%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1178">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1178">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1179">None, valore introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-1179">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1180">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1180">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1181">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1181">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1182">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1182">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1183">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1183">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicGameTasks"></span><span id="folderid_publicgametasks"></span><span id="FOLDERID_PUBLICGAMETASKS"></span><dl> <span data-ttu-id="9c198-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1185">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1185">GUID</span></span></td>
<td><span data-ttu-id="9c198-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span><span class="sxs-lookup"><span data-stu-id="9c198-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1187">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1187">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1188">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="9c198-1188">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1189">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1189">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1190">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1190">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1191">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1191">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1192">%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</span><span class="sxs-lookup"><span data-stu-id="9c198-1192">%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1193">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1193">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1194">None, valore introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-1194">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1195">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1195">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1196">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1196">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1197">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1197">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1198">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1198">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicLibraries"></span><span id="folderid_publiclibraries"></span><span id="FOLDERID_PUBLICLIBRARIES"></span><dl> <span data-ttu-id="9c198-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1200">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1200">GUID</span></span></td>
<td><span data-ttu-id="9c198-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span><span class="sxs-lookup"><span data-stu-id="9c198-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1202">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1202">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1203">Librerie</span><span class="sxs-lookup"><span data-stu-id="9c198-1203">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1204">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1204">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1205">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1205">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1206">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1206">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1207">%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</span><span class="sxs-lookup"><span data-stu-id="9c198-1207">%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1208">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1208">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1209">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-1209">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1210">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1210">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1211">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1211">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1212">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1212">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1213">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1213">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicMusic"></span><span id="folderid_publicmusic"></span><span id="FOLDERID_PUBLICMUSIC"></span><dl> <span data-ttu-id="9c198-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1215">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1215">GUID</span></span></td>
<td><span data-ttu-id="9c198-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span><span class="sxs-lookup"><span data-stu-id="9c198-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1217">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1217">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1218">Musica pubblica</span><span class="sxs-lookup"><span data-stu-id="9c198-1218">Public Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1219">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1219">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1220">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1220">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1221">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1221">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1222">%PUBLIC%\Music</span><span class="sxs-lookup"><span data-stu-id="9c198-1222">%PUBLIC%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1223">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1223">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1224">CSIDL_COMMON_MUSIC</span><span class="sxs-lookup"><span data-stu-id="9c198-1224">CSIDL_COMMON_MUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1225">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1225">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1226">Musica condivisa</span><span class="sxs-lookup"><span data-stu-id="9c198-1226">Shared Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1227">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1227">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1228">Musica%ALLUSERSPROFILE%\Documents\My</span><span class="sxs-lookup"><span data-stu-id="9c198-1228">%ALLUSERSPROFILE%\Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicPictures"></span><span id="folderid_publicpictures"></span><span id="FOLDERID_PUBLICPICTURES"></span><dl> <span data-ttu-id="9c198-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1230">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1230">GUID</span></span></td>
<td><span data-ttu-id="9c198-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span><span class="sxs-lookup"><span data-stu-id="9c198-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1232">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1232">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1233">Immagini pubbliche</span><span class="sxs-lookup"><span data-stu-id="9c198-1233">Public Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1234">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1234">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1235">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1235">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1236">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1236">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1237">%PUBLIC%\Pictures</span><span class="sxs-lookup"><span data-stu-id="9c198-1237">%PUBLIC%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1238">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1238">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1239">CSIDL_COMMON_PICTURES</span><span class="sxs-lookup"><span data-stu-id="9c198-1239">CSIDL_COMMON_PICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1240">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1240">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1241">Immagini condivise</span><span class="sxs-lookup"><span data-stu-id="9c198-1241">Shared Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1242">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1242">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1243">Immagini di%ALLUSERSPROFILE%\Documents\My</span><span class="sxs-lookup"><span data-stu-id="9c198-1243">%ALLUSERSPROFILE%\Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicRingtones"></span><span id="folderid_publicringtones"></span><span id="FOLDERID_PUBLICRINGTONES"></span><dl> <span data-ttu-id="9c198-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1245">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1245">GUID</span></span></td>
<td><span data-ttu-id="9c198-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span><span class="sxs-lookup"><span data-stu-id="9c198-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1247">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1247">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1248">Suonerie</span><span class="sxs-lookup"><span data-stu-id="9c198-1248">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1249">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1249">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1250">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1250">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1251">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1251">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1252">%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</span><span class="sxs-lookup"><span data-stu-id="9c198-1252">%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1253">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1253">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1254">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-1254">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1255">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1255">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1256">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1256">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1257">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1257">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1258">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1258">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicUserTiles"></span><span id="folderid_publicusertiles"></span><span id="FOLDERID_PUBLICUSERTILES"></span><dl> <span data-ttu-id="9c198-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1260">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1260">GUID</span></span></td>
<td><span data-ttu-id="9c198-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span><span class="sxs-lookup"><span data-stu-id="9c198-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1262">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1262">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1263">Immagini di account pubblico</span><span class="sxs-lookup"><span data-stu-id="9c198-1263">Public Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1264">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1264">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1265">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1265">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1266">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1266">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1267">%PUBLIC%\AccountPictures</span><span class="sxs-lookup"><span data-stu-id="9c198-1267">%PUBLIC%\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1268">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1268">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1269">None, valore introdotto in Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c198-1269">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1270">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1270">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1271">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1271">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1272">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1272">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1273">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1273">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicVideos"></span><span id="folderid_publicvideos"></span><span id="FOLDERID_PUBLICVIDEOS"></span><dl> <span data-ttu-id="9c198-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1275">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1275">GUID</span></span></td>
<td><span data-ttu-id="9c198-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span><span class="sxs-lookup"><span data-stu-id="9c198-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1277">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1277">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1278">Video musicali</span><span class="sxs-lookup"><span data-stu-id="9c198-1278">Public Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1279">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1279">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1280">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1280">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1281">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1281">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1282">%PUBLIC%\Videos</span><span class="sxs-lookup"><span data-stu-id="9c198-1282">%PUBLIC%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1283">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1283">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1284">CSIDL_COMMON_VIDEO</span><span class="sxs-lookup"><span data-stu-id="9c198-1284">CSIDL_COMMON_VIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1285">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1285">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1286">Video condiviso</span><span class="sxs-lookup"><span data-stu-id="9c198-1286">Shared Video</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1287">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1287">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1288">Video su%ALLUSERSPROFILE%\Documents\My</span><span class="sxs-lookup"><span data-stu-id="9c198-1288">%ALLUSERSPROFILE%\Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_QuickLaunch"></span><span id="folderid_quicklaunch"></span><span id="FOLDERID_QUICKLAUNCH"></span><dl> <span data-ttu-id="9c198-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1290">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1290">GUID</span></span></td>
<td><span data-ttu-id="9c198-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span><span class="sxs-lookup"><span data-stu-id="9c198-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1292">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1292">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1293">Avvio veloce</span><span class="sxs-lookup"><span data-stu-id="9c198-1293">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1294">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1294">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1295">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1295">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1296">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1296">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1297">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span><span class="sxs-lookup"><span data-stu-id="9c198-1297">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1298">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1298">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1299">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1299">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1300">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1300">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1301">Avvio veloce</span><span class="sxs-lookup"><span data-stu-id="9c198-1301">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1302">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1302">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1303">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span><span class="sxs-lookup"><span data-stu-id="9c198-1303">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Recent"></span><span id="folderid_recent"></span><span id="FOLDERID_RECENT"></span><dl> <span data-ttu-id="9c198-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1305">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1305">GUID</span></span></td>
<td><span data-ttu-id="9c198-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span><span class="sxs-lookup"><span data-stu-id="9c198-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1307">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1307">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1308">Elementi recenti</span><span class="sxs-lookup"><span data-stu-id="9c198-1308">Recent Items</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1309">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1309">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1310">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1310">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1311">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1311">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1312">%APPDATA%\Microsoft\Windows\Recent</span><span class="sxs-lookup"><span data-stu-id="9c198-1312">%APPDATA%\Microsoft\Windows\Recent</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1313">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1313">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1314">CSIDL_RECENT</span><span class="sxs-lookup"><span data-stu-id="9c198-1314">CSIDL_RECENT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1315">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1315">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1316">Documenti recenti</span><span class="sxs-lookup"><span data-stu-id="9c198-1316">My Recent Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1317">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1317">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1318">%USERPROFILE%\Recent</span><span class="sxs-lookup"><span data-stu-id="9c198-1318">%USERPROFILE%\Recent</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecordedTV"></span><span id="folderid_recordedtv"></span><span id="FOLDERID_RECORDEDTV"></span><dl> <span data-ttu-id="9c198-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9c198-1320">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9c198-1320">Not used.</span></span> <span data-ttu-id="9c198-1321">Questo valore non è definito a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9c198-1321">This value is undefined as of Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RecordedTVLibrary"></span><span id="folderid_recordedtvlibrary"></span><span id="FOLDERID_RECORDEDTVLIBRARY"></span><dl> <span data-ttu-id="9c198-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1323">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1323">GUID</span></span></td>
<td><span data-ttu-id="9c198-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span><span class="sxs-lookup"><span data-stu-id="9c198-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1325">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1325">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1326">Registrazioni</span><span class="sxs-lookup"><span data-stu-id="9c198-1326">Recorded TV</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1327">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1327">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1328">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1328">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1329">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1329">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1330">%PUBLIC%\RecordedTV.library-ms</span><span class="sxs-lookup"><span data-stu-id="9c198-1330">%PUBLIC%\RecordedTV.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1331">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1331">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1332">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-1332">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1333">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1333">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1334">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1334">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1335">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1335">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1336">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecycleBinFolder"></span><span id="folderid_recyclebinfolder"></span><span id="FOLDERID_RECYCLEBINFOLDER"></span><dl> <span data-ttu-id="9c198-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1338">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1338">GUID</span></span></td>
<td><span data-ttu-id="9c198-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span><span class="sxs-lookup"><span data-stu-id="9c198-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1340">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1340">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1341">Cestino</span><span class="sxs-lookup"><span data-stu-id="9c198-1341">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1342">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1342">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1343">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-1343">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1344">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1344">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1345">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-1345">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1346">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1346">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1347">CSIDL_BITBUCKET</span><span class="sxs-lookup"><span data-stu-id="9c198-1347">CSIDL_BITBUCKET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1348">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1348">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1349">Cestino</span><span class="sxs-lookup"><span data-stu-id="9c198-1349">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1350">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1350">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1351">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-1351">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ResourceDir"></span><span id="folderid_resourcedir"></span><span id="FOLDERID_RESOURCEDIR"></span><dl> <span data-ttu-id="9c198-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1353">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1353">GUID</span></span></td>
<td><span data-ttu-id="9c198-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span><span class="sxs-lookup"><span data-stu-id="9c198-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1355">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1355">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1356">Risorse</span><span class="sxs-lookup"><span data-stu-id="9c198-1356">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1357">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1357">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1358">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1358">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1359">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1359">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1360">%windir%\Resources</span><span class="sxs-lookup"><span data-stu-id="9c198-1360">%windir%\Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1361">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1361">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1362">CSIDL_RESOURCES</span><span class="sxs-lookup"><span data-stu-id="9c198-1362">CSIDL_RESOURCES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1363">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1363">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1364">Risorse</span><span class="sxs-lookup"><span data-stu-id="9c198-1364">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1365">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1365">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1366">%windir%\Resources</span><span class="sxs-lookup"><span data-stu-id="9c198-1366">%windir%\Resources</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Ringtones"></span><span id="folderid_ringtones"></span><span id="FOLDERID_RINGTONES"></span><dl> <span data-ttu-id="9c198-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1368">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1368">GUID</span></span></td>
<td><span data-ttu-id="9c198-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span><span class="sxs-lookup"><span data-stu-id="9c198-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1370">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1370">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1371">Suonerie</span><span class="sxs-lookup"><span data-stu-id="9c198-1371">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1372">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1372">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1373">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1373">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1374">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1374">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1375">%LOCALAPPDATA%\Microsoft\Windows\Ringtones</span><span class="sxs-lookup"><span data-stu-id="9c198-1375">%LOCALAPPDATA%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1376">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1376">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1377">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-1377">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1378">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1378">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1379">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1379">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1380">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1380">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1381">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1381">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingAppData"></span><span id="folderid_roamingappdata"></span><span id="FOLDERID_ROAMINGAPPDATA"></span><dl> <span data-ttu-id="9c198-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1383">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1383">GUID</span></span></td>
<td><span data-ttu-id="9c198-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span><span class="sxs-lookup"><span data-stu-id="9c198-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1385">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1385">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1386">Roaming</span><span class="sxs-lookup"><span data-stu-id="9c198-1386">Roaming</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1387">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1387">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1388">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1388">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1389">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1389">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1390">% APPDATA% (%USERPROFILE%\AppData\Roaming)</span><span class="sxs-lookup"><span data-stu-id="9c198-1390">%APPDATA% (%USERPROFILE%\AppData\Roaming)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1391">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1391">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1392">CSIDL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="9c198-1392">CSIDL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1393">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1393">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1394">Dati applicazione</span><span class="sxs-lookup"><span data-stu-id="9c198-1394">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1395">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1395">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1396">% APPDATA% (dati%USERPROFILE%\Application)</span><span class="sxs-lookup"><span data-stu-id="9c198-1396">%APPDATA% (%USERPROFILE%\Application Data)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RoamedTileImages"></span><span id="folderid_roamedtileimages"></span><span id="FOLDERID_ROAMEDTILEIMAGES"></span><dl> <span data-ttu-id="9c198-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1398">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1398">GUID</span></span></td>
<td><span data-ttu-id="9c198-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span><span class="sxs-lookup"><span data-stu-id="9c198-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1400">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1400">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1401">RoamedTileImages</span><span class="sxs-lookup"><span data-stu-id="9c198-1401">RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1402">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1402">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1403">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1403">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1404">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1404">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1405">%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</span><span class="sxs-lookup"><span data-stu-id="9c198-1405">%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1406">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1406">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1407">None, valore introdotto in Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c198-1407">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1408">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1408">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1409">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1409">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1410">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1410">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1411">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1411">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingTiles"></span><span id="folderid_roamingtiles"></span><span id="FOLDERID_ROAMINGTILES"></span><dl> <span data-ttu-id="9c198-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1413">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1413">GUID</span></span></td>
<td><span data-ttu-id="9c198-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span><span class="sxs-lookup"><span data-stu-id="9c198-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1415">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1415">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1416">RoamingTiles</span><span class="sxs-lookup"><span data-stu-id="9c198-1416">RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1417">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1417">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1418">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1418">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1419">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1419">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1420">%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</span><span class="sxs-lookup"><span data-stu-id="9c198-1420">%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1421">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1421">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1422">None, valore introdotto in Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c198-1422">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1423">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1423">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1424">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1424">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1425">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1425">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1426">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1426">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SampleMusic"></span><span id="folderid_samplemusic"></span><span id="FOLDERID_SAMPLEMUSIC"></span><dl> <span data-ttu-id="9c198-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1428">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1428">GUID</span></span></td>
<td><span data-ttu-id="9c198-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span><span class="sxs-lookup"><span data-stu-id="9c198-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1430">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1430">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1431">Musica di esempio</span><span class="sxs-lookup"><span data-stu-id="9c198-1431">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1432">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1432">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1433">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1433">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1434">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1434">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1435">Musica%PUBLIC%\Music\Sample</span><span class="sxs-lookup"><span data-stu-id="9c198-1435">%PUBLIC%\Music\Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1436">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1436">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1437">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1437">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1438">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1438">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1439">Musica di esempio</span><span class="sxs-lookup"><span data-stu-id="9c198-1439">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1440">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1440">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1441">Musica%ALLUSERSPROFILE%\Documents\My Music\Sample</span><span class="sxs-lookup"><span data-stu-id="9c198-1441">%ALLUSERSPROFILE%\Documents\My Music\Sample Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SamplePictures"></span><span id="folderid_samplepictures"></span><span id="FOLDERID_SAMPLEPICTURES"></span><dl> <span data-ttu-id="9c198-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1443">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1443">GUID</span></span></td>
<td><span data-ttu-id="9c198-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span><span class="sxs-lookup"><span data-stu-id="9c198-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1445">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1445">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1446">Immagini di esempio</span><span class="sxs-lookup"><span data-stu-id="9c198-1446">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1447">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1447">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1448">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1448">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1449">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1449">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1450">Immagini di%PUBLIC%\Pictures\Sample</span><span class="sxs-lookup"><span data-stu-id="9c198-1450">%PUBLIC%\Pictures\Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1451">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1451">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1452">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1452">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1453">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1453">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1454">Immagini di esempio</span><span class="sxs-lookup"><span data-stu-id="9c198-1454">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1455">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1455">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1456">Immagini di%ALLUSERSPROFILE%\Documents\My Immagini\immagini</span><span class="sxs-lookup"><span data-stu-id="9c198-1456">%ALLUSERSPROFILE%\Documents\My Pictures\Sample Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SamplePlaylists"></span><span id="folderid_sampleplaylists"></span><span id="FOLDERID_SAMPLEPLAYLISTS"></span><dl> <span data-ttu-id="9c198-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1458">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1458">GUID</span></span></td>
<td><span data-ttu-id="9c198-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span><span class="sxs-lookup"><span data-stu-id="9c198-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1460">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1460">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1461">Playlist di esempio</span><span class="sxs-lookup"><span data-stu-id="9c198-1461">Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1462">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1462">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1463">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1463">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1464">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1464">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1465">%PUBLIC%\Music\Sample playlist</span><span class="sxs-lookup"><span data-stu-id="9c198-1465">%PUBLIC%\Music\Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1466">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1466">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1467">None, valore introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-1467">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1468">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1468">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1469">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1469">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1470">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1470">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1471">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1471">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SampleVideos"></span><span id="folderid_samplevideos"></span><span id="FOLDERID_SAMPLEVIDEOS"></span><dl> <span data-ttu-id="9c198-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1473">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1473">GUID</span></span></td>
<td><span data-ttu-id="9c198-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span><span class="sxs-lookup"><span data-stu-id="9c198-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1475">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1475">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1476">Video di esempio</span><span class="sxs-lookup"><span data-stu-id="9c198-1476">Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1477">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1477">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1478">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1478">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1479">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1479">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1480">Video su%PUBLIC%\Videos\Sample</span><span class="sxs-lookup"><span data-stu-id="9c198-1480">%PUBLIC%\Videos\Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1481">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1481">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1482">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1482">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1483">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1483">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1484">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1484">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1485">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1485">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1486">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1486">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedGames"></span><span id="folderid_savedgames"></span><span id="FOLDERID_SAVEDGAMES"></span><dl> <span data-ttu-id="9c198-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1488">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1488">GUID</span></span></td>
<td><span data-ttu-id="9c198-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span><span class="sxs-lookup"><span data-stu-id="9c198-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1490">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1490">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1491">Partite salvate</span><span class="sxs-lookup"><span data-stu-id="9c198-1491">Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1492">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1492">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1493">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1493">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1494">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1494">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1495">Giochi%USERPROFILE%\Saved</span><span class="sxs-lookup"><span data-stu-id="9c198-1495">%USERPROFILE%\Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1496">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1496">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1497">None, valore introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-1497">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1498">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1498">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1499">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1499">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1500">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1500">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1501">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1501">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedPictures"></span><span id="folderid_savedpictures"></span><span id="FOLDERID_SAVEDPICTURES"></span><dl> <span data-ttu-id="9c198-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1503">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1503">GUID</span></span></td>
<td><span data-ttu-id="9c198-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span><span class="sxs-lookup"><span data-stu-id="9c198-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1505">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1505">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1506">Immagini salvate</span><span class="sxs-lookup"><span data-stu-id="9c198-1506">Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1507">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1507">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1508">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1508">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1509">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1509">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1510">Immagini di%USERPROFILE%\Pictures\Saved</span><span class="sxs-lookup"><span data-stu-id="9c198-1510">%USERPROFILE%\Pictures\Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1511">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1511">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1512">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1512">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1513">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1513">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1514">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1514">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1515">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1515">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1516">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1516">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedPicturesLibrary"></span><span id="folderid_savedpictureslibrary"></span><span id="FOLDERID_SAVEDPICTURESLIBRARY"></span><dl> <span data-ttu-id="9c198-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1518">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1518">GUID</span></span></td>
<td><span data-ttu-id="9c198-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span><span class="sxs-lookup"><span data-stu-id="9c198-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1520">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1520">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1521">Libreria immagini salvate</span><span class="sxs-lookup"><span data-stu-id="9c198-1521">Saved Pictures Library</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1522">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1522">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1523">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1523">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1524">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1524">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1525">%APPDATE%\Microsoft\Windows\Libraries\SavedPictures.library-ms</span><span class="sxs-lookup"><span data-stu-id="9c198-1525">%APPDATE%\Microsoft\Windows\Libraries\SavedPictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1526">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1526">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1527">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1527">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1528">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1528">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1529">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1529">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1530">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1530">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1531">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1531">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedSearches"></span><span id="folderid_savedsearches"></span><span id="FOLDERID_SAVEDSEARCHES"></span><dl> <span data-ttu-id="9c198-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1533">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1533">GUID</span></span></td>
<td><span data-ttu-id="9c198-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span><span class="sxs-lookup"><span data-stu-id="9c198-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1535">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1535">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1536">Ricerche</span><span class="sxs-lookup"><span data-stu-id="9c198-1536">Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1537">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1537">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1538">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1538">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1539">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1539">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1540">%USERPROFILE%\Searches</span><span class="sxs-lookup"><span data-stu-id="9c198-1540">%USERPROFILE%\Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1541">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1541">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1542">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1542">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1543">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1543">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1544">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1544">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1545">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1545">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1546">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1546">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Screenshots"></span><span id="folderid_screenshots"></span><span id="FOLDERID_SCREENSHOTS"></span><dl> <span data-ttu-id="9c198-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1548">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1548">GUID</span></span></td>
<td><span data-ttu-id="9c198-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span><span class="sxs-lookup"><span data-stu-id="9c198-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1550">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1550">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1551">Schermate</span><span class="sxs-lookup"><span data-stu-id="9c198-1551">Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1552">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1552">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1553">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1553">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1554">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1554">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1555">%USERPROFILE%\Pictures\Screenshots</span><span class="sxs-lookup"><span data-stu-id="9c198-1555">%USERPROFILE%\Pictures\Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1556">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1556">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1557">None, valore introdotto in Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c198-1557">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1558">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1558">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1559">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1559">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1560">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1560">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1561">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1561">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_CSC"></span><span id="folderid_search_csc"></span><dl> <span data-ttu-id="9c198-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1563">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1563">GUID</span></span></td>
<td><span data-ttu-id="9c198-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span><span class="sxs-lookup"><span data-stu-id="9c198-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1565">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1565">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1566">File offline</span><span class="sxs-lookup"><span data-stu-id="9c198-1566">Offline Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1567">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1567">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1568">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-1568">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1569">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1569">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1570">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-1570">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1571">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1571">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1572">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1572">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1573">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1573">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1574">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1574">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1575">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1575">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1576">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1576">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SearchHistory"></span><span id="folderid_searchhistory"></span><span id="FOLDERID_SEARCHHISTORY"></span><dl> <span data-ttu-id="9c198-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1578">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1578">GUID</span></span></td>
<td><span data-ttu-id="9c198-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span><span class="sxs-lookup"><span data-stu-id="9c198-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1580">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1580">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1581">Cronologia</span><span class="sxs-lookup"><span data-stu-id="9c198-1581">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1582">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1582">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1583">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1583">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1584">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1584">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1585">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</span><span class="sxs-lookup"><span data-stu-id="9c198-1585">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1586">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1586">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1587">None, valore introdotto in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9c198-1587">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1588">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1588">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1589">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1589">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1590">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1590">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1591">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1591">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchHome"></span><span id="folderid_searchhome"></span><span id="FOLDERID_SEARCHHOME"></span><dl> <span data-ttu-id="9c198-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1593">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1593">GUID</span></span></td>
<td><span data-ttu-id="9c198-1594">{190337d1-B8CA-4121-A639-6d472d16972a}</span><span class="sxs-lookup"><span data-stu-id="9c198-1594">{190337d1-b8ca-4121-a639-6d472d16972a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1595">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1595">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1596">Risultati della ricerca</span><span class="sxs-lookup"><span data-stu-id="9c198-1596">Search Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1597">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1597">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1598">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-1598">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1599">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1599">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1600">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-1600">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1601">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1601">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1602">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1602">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1603">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1603">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1604">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1604">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1605">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1605">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1606">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1606">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_MAPI"></span><span id="folderid_search_mapi"></span><dl> <span data-ttu-id="9c198-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1608">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1608">GUID</span></span></td>
<td><span data-ttu-id="9c198-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span><span class="sxs-lookup"><span data-stu-id="9c198-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1610">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1610">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1611">Microsoft Office Outlook</span><span class="sxs-lookup"><span data-stu-id="9c198-1611">Microsoft Office Outlook</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1612">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1612">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1613">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-1613">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1614">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1614">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1615">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-1615">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1616">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1616">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1617">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1617">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1618">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1618">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1619">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1619">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1620">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1620">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1621">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1621">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchTemplates"></span><span id="folderid_searchtemplates"></span><span id="FOLDERID_SEARCHTEMPLATES"></span><dl> <span data-ttu-id="9c198-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1623">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1623">GUID</span></span></td>
<td><span data-ttu-id="9c198-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span><span class="sxs-lookup"><span data-stu-id="9c198-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1625">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1625">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1626">Modelli</span><span class="sxs-lookup"><span data-stu-id="9c198-1626">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1627">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1627">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1628">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1628">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1629">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1629">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1630">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</span><span class="sxs-lookup"><span data-stu-id="9c198-1630">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1631">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1631">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1632">None, valore introdotto in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9c198-1632">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1633">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1633">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1634">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1634">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1635">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1635">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1636">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1636">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SendTo"></span><span id="folderid_sendto"></span><span id="FOLDERID_SENDTO"></span><dl> <span data-ttu-id="9c198-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1638">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1638">GUID</span></span></td>
<td><span data-ttu-id="9c198-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span><span class="sxs-lookup"><span data-stu-id="9c198-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1640">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1640">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1641">SendTo</span><span class="sxs-lookup"><span data-stu-id="9c198-1641">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1642">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1642">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1643">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1643">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1644">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1644">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1645">%APPDATA%\Microsoft\Windows\SendTo</span><span class="sxs-lookup"><span data-stu-id="9c198-1645">%APPDATA%\Microsoft\Windows\SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1646">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1646">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1647">CSIDL_SENDTO</span><span class="sxs-lookup"><span data-stu-id="9c198-1647">CSIDL_SENDTO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1648">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1648">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1649">SendTo</span><span class="sxs-lookup"><span data-stu-id="9c198-1649">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1650">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1650">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1651">%USERPROFILE%\SendTo</span><span class="sxs-lookup"><span data-stu-id="9c198-1651">%USERPROFILE%\SendTo</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SidebarDefaultParts"></span><span id="folderid_sidebardefaultparts"></span><span id="FOLDERID_SIDEBARDEFAULTPARTS"></span><dl> <span data-ttu-id="9c198-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1653">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1653">GUID</span></span></td>
<td><span data-ttu-id="9c198-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span><span class="sxs-lookup"><span data-stu-id="9c198-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1655">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1655">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1656">Gadget</span><span class="sxs-lookup"><span data-stu-id="9c198-1656">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1657">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1657">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1658">COMUNE</span><span class="sxs-lookup"><span data-stu-id="9c198-1658">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1659">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1659">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1660">Sidebar\Gadgets%programmi%\Windows</span><span class="sxs-lookup"><span data-stu-id="9c198-1660">%ProgramFiles%\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1661">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1661">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1662">Nessuno, nuovo per Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-1662">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1663">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1663">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1664">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1664">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1665">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1665">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1666">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1666">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SidebarParts"></span><span id="folderid_sidebarparts"></span><span id="FOLDERID_SIDEBARPARTS"></span><dl> <span data-ttu-id="9c198-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1668">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1668">GUID</span></span></td>
<td><span data-ttu-id="9c198-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span><span class="sxs-lookup"><span data-stu-id="9c198-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1670">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1670">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1671">Gadget</span><span class="sxs-lookup"><span data-stu-id="9c198-1671">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1672">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1672">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1673">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1673">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1674">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1674">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1675">%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets</span><span class="sxs-lookup"><span data-stu-id="9c198-1675">%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1676">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1676">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1677">Nessuno, nuovo per Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-1677">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1678">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1678">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1679">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1679">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1680">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1680">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1681">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1681">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDrive"></span><span id="folderid_skydrive"></span><span id="FOLDERID_SKYDRIVE"></span><dl> <span data-ttu-id="9c198-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1683">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1683">GUID</span></span></td>
<td><span data-ttu-id="9c198-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span><span class="sxs-lookup"><span data-stu-id="9c198-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1685">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1685">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1686">OneDrive</span><span class="sxs-lookup"><span data-stu-id="9c198-1686">OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1687">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1687">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1688">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1688">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1689">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1689">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1690">%USERPROFILE%\OneDrive</span><span class="sxs-lookup"><span data-stu-id="9c198-1690">%USERPROFILE%\OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1691">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1691">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1692">None, valore introdotto in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9c198-1692">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1693">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1693">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1694">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1694">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1695">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1695">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1696">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1696">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveCameraRoll"></span><span id="folderid_skydrivecameraroll"></span><span id="FOLDERID_SKYDRIVECAMERAROLL"></span><dl> <span data-ttu-id="9c198-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1698">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1698">GUID</span></span></td>
<td><span data-ttu-id="9c198-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span><span class="sxs-lookup"><span data-stu-id="9c198-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1700">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1700">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1701">Rullo della fotocamera</span><span class="sxs-lookup"><span data-stu-id="9c198-1701">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1702">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1702">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1703">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1703">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1704">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1704">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1705">%USERPROFILE%\OneDrive\Pictures\Camera roll</span><span class="sxs-lookup"><span data-stu-id="9c198-1705">%USERPROFILE%\OneDrive\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1706">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1706">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1707">None, valore introdotto in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9c198-1707">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1708">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1708">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1709">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1709">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1710">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1710">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1711">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1711">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveDocuments"></span><span id="folderid_skydrivedocuments"></span><span id="FOLDERID_SKYDRIVEDOCUMENTS"></span><dl> <span data-ttu-id="9c198-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1713">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1713">GUID</span></span></td>
<td><span data-ttu-id="9c198-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span><span class="sxs-lookup"><span data-stu-id="9c198-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1715">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1715">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1716">Documenti</span><span class="sxs-lookup"><span data-stu-id="9c198-1716">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1717">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1717">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1718">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1718">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1719">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1719">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1720">%USERPROFILE%\OneDrive\Documents</span><span class="sxs-lookup"><span data-stu-id="9c198-1720">%USERPROFILE%\OneDrive\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1721">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1721">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1722">None, valore introdotto in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9c198-1722">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1723">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1723">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1724">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1724">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1725">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1725">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1726">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1726">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDrivePictures"></span><span id="folderid_skydrivepictures"></span><span id="FOLDERID_SKYDRIVEPICTURES"></span><dl> <span data-ttu-id="9c198-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1728">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1728">GUID</span></span></td>
<td><span data-ttu-id="9c198-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span><span class="sxs-lookup"><span data-stu-id="9c198-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1730">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1730">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1731">Immagini</span><span class="sxs-lookup"><span data-stu-id="9c198-1731">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1732">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1732">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1733">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1733">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1734">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1734">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1735">%USERPROFILE%\OneDrive\Pictures</span><span class="sxs-lookup"><span data-stu-id="9c198-1735">%USERPROFILE%\OneDrive\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1736">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1736">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1737">None, valore introdotto in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9c198-1737">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1738">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1738">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1739">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1739">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1740">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1740">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1741">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1741">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_StartMenu"></span><span id="folderid_startmenu"></span><span id="FOLDERID_STARTMENU"></span><dl> <span data-ttu-id="9c198-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1743">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1743">GUID</span></span></td>
<td><span data-ttu-id="9c198-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span><span class="sxs-lookup"><span data-stu-id="9c198-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1745">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1745">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1746">Menu Start</span><span class="sxs-lookup"><span data-stu-id="9c198-1746">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1747">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1747">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1748">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1748">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1749">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1749">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1750">Menu%APPDATA%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="9c198-1750">%APPDATA%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1751">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1751">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1752">CSIDL_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="9c198-1752">CSIDL_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1753">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1753">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1754">Menu Start</span><span class="sxs-lookup"><span data-stu-id="9c198-1754">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1755">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1755">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1756">Menu%USERPROFILE%\Menu</span><span class="sxs-lookup"><span data-stu-id="9c198-1756">%USERPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Startup"></span><span id="folderid_startup"></span><span id="FOLDERID_STARTUP"></span><dl> <span data-ttu-id="9c198-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1758">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1758">GUID</span></span></td>
<td><span data-ttu-id="9c198-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span><span class="sxs-lookup"><span data-stu-id="9c198-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1760">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1760">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1761">Avvio</span><span class="sxs-lookup"><span data-stu-id="9c198-1761">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1762">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1762">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1763">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1763">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1764">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1764">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1765">Avvio\programmi\esecuzione automatica%APPDATA%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="9c198-1765">%APPDATA%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1766">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1766">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1767">CSIDL_STARTUP, CSIDL_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="9c198-1767">CSIDL_STARTUP, CSIDL_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1768">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1768">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1769">Avvio</span><span class="sxs-lookup"><span data-stu-id="9c198-1769">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1770">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1770">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1771">Avvio\programmi\esecuzione automatica%USERPROFILE%\Menu</span><span class="sxs-lookup"><span data-stu-id="9c198-1771">%USERPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncManagerFolder"></span><span id="folderid_syncmanagerfolder"></span><span id="FOLDERID_SYNCMANAGERFOLDER"></span><dl> <span data-ttu-id="9c198-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1773">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1773">GUID</span></span></td>
<td><span data-ttu-id="9c198-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span><span class="sxs-lookup"><span data-stu-id="9c198-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1775">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1775">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1776">Centro sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="9c198-1776">Sync Center</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1777">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1777">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1778">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-1778">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1779">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1779">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1780">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-1780">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1781">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1781">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1782">None, valore introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-1782">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1783">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1783">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1784">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1784">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1785">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1785">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1786">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1786">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SyncResultsFolder"></span><span id="folderid_syncresultsfolder"></span><span id="FOLDERID_SYNCRESULTSFOLDER"></span><dl> <span data-ttu-id="9c198-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1788">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1788">GUID</span></span></td>
<td><span data-ttu-id="9c198-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span><span class="sxs-lookup"><span data-stu-id="9c198-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1790">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1790">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1791">Risultati sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="9c198-1791">Sync Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1792">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1792">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1793">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-1793">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1794">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1794">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1795">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-1795">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1796">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1796">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1797">None, valore introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-1797">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1798">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1798">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1799">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1799">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1800">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1800">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1801">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1801">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncSetupFolder"></span><span id="folderid_syncsetupfolder"></span><span id="FOLDERID_SYNCSETUPFOLDER"></span><dl> <span data-ttu-id="9c198-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1803">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1803">GUID</span></span></td>
<td><span data-ttu-id="9c198-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span><span class="sxs-lookup"><span data-stu-id="9c198-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1805">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1805">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1806">Configurazione della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="9c198-1806">Sync Setup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1807">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1807">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1808">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-1808">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1809">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1809">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1810">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-1810">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1811">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1811">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1812">None, valore introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-1812">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1813">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1813">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1814">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1814">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1815">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1815">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1816">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1816">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_System"></span><span id="folderid_system"></span><span id="FOLDERID_SYSTEM"></span><dl> <span data-ttu-id="9c198-1817"><dt><strong>FOLDERID_System</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1817"><dt><strong>FOLDERID_System</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1818">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1818">GUID</span></span></td>
<td><span data-ttu-id="9c198-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span><span class="sxs-lookup"><span data-stu-id="9c198-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1820">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1820">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1821">System32</span><span class="sxs-lookup"><span data-stu-id="9c198-1821">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1822">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1822">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1823">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1823">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1824">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1824">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1825">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="9c198-1825">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1826">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1826">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1827">CSIDL_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="9c198-1827">CSIDL_SYSTEM</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1828">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1828">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1829">system32</span><span class="sxs-lookup"><span data-stu-id="9c198-1829">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1830">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1830">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1831">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="9c198-1831">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SystemX86"></span><span id="folderid_systemx86"></span><span id="FOLDERID_SYSTEMX86"></span><dl> <span data-ttu-id="9c198-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1833">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1833">GUID</span></span></td>
<td><span data-ttu-id="9c198-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span><span class="sxs-lookup"><span data-stu-id="9c198-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1835">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1835">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1836">System32</span><span class="sxs-lookup"><span data-stu-id="9c198-1836">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1837">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1837">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1838">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1838">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1839">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1839">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1840">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="9c198-1840">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1841">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1841">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1842">CSIDL_SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="9c198-1842">CSIDL_SYSTEMX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1843">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1843">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1844">system32</span><span class="sxs-lookup"><span data-stu-id="9c198-1844">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1845">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1845">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1846">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="9c198-1846">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Templates"></span><span id="folderid_templates"></span><span id="FOLDERID_TEMPLATES"></span><dl> <span data-ttu-id="9c198-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1848">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1848">GUID</span></span></td>
<td><span data-ttu-id="9c198-1849">A63293E8-664E-48DB-A079-DF759E0509F7</span><span class="sxs-lookup"><span data-stu-id="9c198-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1850">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1850">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1851">Modelli</span><span class="sxs-lookup"><span data-stu-id="9c198-1851">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1852">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1852">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1853">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1853">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1854">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1854">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1855">%APPDATA%\Microsoft\Windows\Templates</span><span class="sxs-lookup"><span data-stu-id="9c198-1855">%APPDATA%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1856">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1856">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1857">CSIDL_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="9c198-1857">CSIDL_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1858">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1858">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1859">Modelli</span><span class="sxs-lookup"><span data-stu-id="9c198-1859">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1860">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1860">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1861">%USERPROFILE%\Templates</span><span class="sxs-lookup"><span data-stu-id="9c198-1861">%USERPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_TreeProperties"></span><span id="folderid_treeproperties"></span><span id="FOLDERID_TREEPROPERTIES"></span><dl> <span data-ttu-id="9c198-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9c198-1863">Non utilizzato in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9c198-1863">Not used in Windows Vista.</span></span> <span data-ttu-id="9c198-1864">Non supportato a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9c198-1864">Unsupported as of Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserPinned"></span><span id="folderid_userpinned"></span><span id="FOLDERID_USERPINNED"></span><dl> <span data-ttu-id="9c198-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1866">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1866">GUID</span></span></td>
<td><span data-ttu-id="9c198-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span><span class="sxs-lookup"><span data-stu-id="9c198-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1868">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1868">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1869">Utente aggiunto</span><span class="sxs-lookup"><span data-stu-id="9c198-1869">User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1870">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1870">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1871">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1871">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1872">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1872">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1873">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User aggiunto</span><span class="sxs-lookup"><span data-stu-id="9c198-1873">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1874">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1874">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1875">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-1875">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1876">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1876">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1877">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1877">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1878">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1878">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1879">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1879">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProfiles"></span><span id="folderid_userprofiles"></span><span id="FOLDERID_USERPROFILES"></span><dl> <span data-ttu-id="9c198-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1881">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1881">GUID</span></span></td>
<td><span data-ttu-id="9c198-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span><span class="sxs-lookup"><span data-stu-id="9c198-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1883">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1883">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1884">Utenti</span><span class="sxs-lookup"><span data-stu-id="9c198-1884">Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1885">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1885">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1886">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1886">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1887">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1887">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1888">%SystemDrive%\Users</span><span class="sxs-lookup"><span data-stu-id="9c198-1888">%SystemDrive%\Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1889">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1889">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1890">Nessuno, nuovo per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c198-1890">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1891">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1891">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1892">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1892">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1893">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1893">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1894">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1894">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFiles"></span><span id="folderid_userprogramfiles"></span><span id="FOLDERID_USERPROGRAMFILES"></span><dl> <span data-ttu-id="9c198-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1896">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1896">GUID</span></span></td>
<td><span data-ttu-id="9c198-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span><span class="sxs-lookup"><span data-stu-id="9c198-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1898">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1898">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1899">Programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-1899">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1900">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1900">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1901">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1901">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1902">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1902">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1903">%LOCALAPPDATA%\Programs</span><span class="sxs-lookup"><span data-stu-id="9c198-1903">%LOCALAPPDATA%\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1904">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1904">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1905">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-1905">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1906">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1906">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1907">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1907">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1908">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1908">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1909">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1909">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFilesCommon"></span><span id="folderid_userprogramfilescommon"></span><span id="FOLDERID_USERPROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="9c198-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1911">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1911">GUID</span></span></td>
<td><span data-ttu-id="9c198-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span><span class="sxs-lookup"><span data-stu-id="9c198-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1913">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1913">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1914">Programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-1914">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1915">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1915">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1916">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1916">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1917">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1917">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1918">%LOCALAPPDATA%\Programs\Common</span><span class="sxs-lookup"><span data-stu-id="9c198-1918">%LOCALAPPDATA%\Programs\Common</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1919">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1919">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1920">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-1920">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1921">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1921">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1922">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1922">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1923">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1923">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1924">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1924">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UsersFiles"></span><span id="folderid_usersfiles"></span><span id="FOLDERID_USERSFILES"></span><dl> <span data-ttu-id="9c198-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1926">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1926">GUID</span></span></td>
<td><span data-ttu-id="9c198-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span><span class="sxs-lookup"><span data-stu-id="9c198-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1928">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1928">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1929">Nome completo dell'utente (ad esempio, Jean Philippe bagel) immesso al momento della creazione dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="9c198-1929">The user's full name (for instance, Jean Philippe Bagel) entered when the user account was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1930">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1930">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1931">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-1931">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1932">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1932">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1933">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-1933">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1934">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1934">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1935">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-1935">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1936">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1936">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1937">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1937">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1938">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1938">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1939">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1939">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UsersLibraries"></span><span id="folderid_userslibraries"></span><span id="FOLDERID_USERSLIBRARIES"></span><dl> <span data-ttu-id="9c198-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1941">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1941">GUID</span></span></td>
<td><span data-ttu-id="9c198-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span><span class="sxs-lookup"><span data-stu-id="9c198-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1943">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1943">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1944">Librerie</span><span class="sxs-lookup"><span data-stu-id="9c198-1944">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1945">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1945">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1946">VIRTUALE</span><span class="sxs-lookup"><span data-stu-id="9c198-1946">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1947">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1947">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1948">Non applicabile: cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="9c198-1948">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1949">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1949">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1950">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-1950">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1951">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1951">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1952">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1952">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1953">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1953">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1954">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1954">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Videos"></span><span id="folderid_videos"></span><span id="FOLDERID_VIDEOS"></span><dl> <span data-ttu-id="9c198-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1956">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1956">GUID</span></span></td>
<td><span data-ttu-id="9c198-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span><span class="sxs-lookup"><span data-stu-id="9c198-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1958">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1958">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1959">Video</span><span class="sxs-lookup"><span data-stu-id="9c198-1959">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1960">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1960">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1961">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1961">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1962">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1962">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1963">%USERPROFILE%\Videos</span><span class="sxs-lookup"><span data-stu-id="9c198-1963">%USERPROFILE%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1964">CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1964">CSIDL</span></span></td>
<td><span data-ttu-id="9c198-1965">CSIDL_MYVIDEO</span><span class="sxs-lookup"><span data-stu-id="9c198-1965">CSIDL_MYVIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1966">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1966">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1967">Video personali</span><span class="sxs-lookup"><span data-stu-id="9c198-1967">My Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1968">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1968">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1969">Video su%USERPROFILE%\My</span><span class="sxs-lookup"><span data-stu-id="9c198-1969">%USERPROFILE%\My Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_VideosLibrary"></span><span id="folderid_videoslibrary"></span><span id="FOLDERID_VIDEOSLIBRARY"></span><dl> <span data-ttu-id="9c198-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1971">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1971">GUID</span></span></td>
<td><span data-ttu-id="9c198-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span><span class="sxs-lookup"><span data-stu-id="9c198-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1973">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1973">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1974">Video</span><span class="sxs-lookup"><span data-stu-id="9c198-1974">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1975">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1975">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1976">PERUSER</span><span class="sxs-lookup"><span data-stu-id="9c198-1976">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1977">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1977">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1978">%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</span><span class="sxs-lookup"><span data-stu-id="9c198-1978">%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1979">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1979">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1980">None, valore introdotto in Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c198-1980">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1981">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1981">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1982">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1982">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1983">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1983">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1984">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-1984">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Windows"></span><span id="folderid_windows"></span><span id="FOLDERID_WINDOWS"></span><dl> <span data-ttu-id="9c198-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9c198-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c198-1986">GUID</span><span class="sxs-lookup"><span data-stu-id="9c198-1986">GUID</span></span></td>
<td><span data-ttu-id="9c198-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span><span class="sxs-lookup"><span data-stu-id="9c198-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1988">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9c198-1988">Display Name</span></span></td>
<td><span data-ttu-id="9c198-1989">Windows</span><span class="sxs-lookup"><span data-stu-id="9c198-1989">Windows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1990">Tipo di cartella</span><span class="sxs-lookup"><span data-stu-id="9c198-1990">Folder Type</span></span></td>
<td><span data-ttu-id="9c198-1991">FIXED</span><span class="sxs-lookup"><span data-stu-id="9c198-1991">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1992">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-1992">Default Path</span></span></td>
<td><span data-ttu-id="9c198-1993">WINDIR</span><span class="sxs-lookup"><span data-stu-id="9c198-1993">%windir%</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1994">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-1994">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9c198-1995">CSIDL_WINDOWS</span><span class="sxs-lookup"><span data-stu-id="9c198-1995">CSIDL_WINDOWS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c198-1996">Nome visualizzato legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1996">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9c198-1997">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="9c198-1997">WINDOWS</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c198-1998">Percorso predefinito legacy</span><span class="sxs-lookup"><span data-stu-id="9c198-1998">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9c198-1999">WINDIR</span><span class="sxs-lookup"><span data-stu-id="9c198-1999">%windir%</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="9c198-2000">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c198-2000">Remarks</span></span>

<span data-ttu-id="9c198-2001">L'interpretazione di determinati valori di **KNOWNFOLDERID** varia a seconda che la cartella faccia parte di un'applicazione a 32 bit o a 64 bit e che l'applicazione sia in esecuzione in un sistema operativo a 32 bit o a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9c198-2001">The interpretation of certain **KNOWNFOLDERID** values depends on whether the folder is part of a 32-bit or 64-bit application and whether that application is running on a 32-bit or 64-bit operating system.</span></span> <span data-ttu-id="9c198-2002">Se l'applicazione deve distinguere tra, ad esempio, **i file di programma** e **programmi (x86)**, è necessario usare il **KNOWNFOLDERID** corretto per la situazione.</span><span class="sxs-lookup"><span data-stu-id="9c198-2002">If your application needs to distinguish between, for example, **Program Files** and **Program Files (x86)**, you must use the right **KNOWNFOLDERID** for the situation.</span></span>

<span data-ttu-id="9c198-2003">Le tabelle seguenti riepilogano l'uso di **KNOWNFOLDERID** in tali casi.</span><span class="sxs-lookup"><span data-stu-id="9c198-2003">The following tables summarize the **KNOWNFOLDERID** use in those cases.</span></span>


<span data-ttu-id="9c198-2004">**\_Programmi FOLDERID**</span><span class="sxs-lookup"><span data-stu-id="9c198-2004">**FOLDERID\_ProgramFiles**</span></span> 

| <span data-ttu-id="9c198-2005">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9c198-2005">Operating System</span></span> | <span data-ttu-id="9c198-2006">Applicazione</span><span class="sxs-lookup"><span data-stu-id="9c198-2006">Application</span></span> | <span data-ttu-id="9c198-2007">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2007">KNOWNFOLDERID</span></span> | <span data-ttu-id="9c198-2008">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-2008">Default Path</span></span> | <span data-ttu-id="9c198-2009">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-2009">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="9c198-2010">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2010">32 bit</span></span> | <span data-ttu-id="9c198-2011">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2011">32 bit</span></span> | <span data-ttu-id="9c198-2012">\_Programmi FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2012">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="9c198-2013">% File di programma% SystemDrive% \\</span><span class="sxs-lookup"><span data-stu-id="9c198-2013">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="9c198-2014">\_file di programma CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="9c198-2014">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="9c198-2015">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2015">32 bit</span></span> | <span data-ttu-id="9c198-2016">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2016">32 bit</span></span> | <span data-ttu-id="9c198-2017">\_PROGRAMFILESX86 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2017">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="9c198-2018">% File di programma% SystemDrive% \\</span><span class="sxs-lookup"><span data-stu-id="9c198-2018">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="9c198-2019">\_Programma CSIDL \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="9c198-2019">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="9c198-2020">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2020">32 bit</span></span> | <span data-ttu-id="9c198-2021">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2021">32 bit</span></span> | <span data-ttu-id="9c198-2022">FOLDERID \_ ProgramFilesX64 (non supportato nei sistemi operativi a 32 bit)</span><span class="sxs-lookup"><span data-stu-id="9c198-2022">FOLDERID\_ProgramFilesX64 (not supported under 32-bit operating systems)</span></span> | <span data-ttu-id="9c198-2023">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-2023">Not applicable</span></span> | <span data-ttu-id="9c198-2024">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-2024">Not applicable</span></span> |
| <span data-ttu-id="9c198-2025">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2025">64 bit</span></span> | <span data-ttu-id="9c198-2026">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2026">64 bit</span></span> | <span data-ttu-id="9c198-2027">\_Programmi FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2027">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="9c198-2028">% File di programma% SystemDrive% \\</span><span class="sxs-lookup"><span data-stu-id="9c198-2028">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="9c198-2029">\_file di programma CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="9c198-2029">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="9c198-2030">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2030">64 bit</span></span> | <span data-ttu-id="9c198-2031">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2031">64 bit</span></span> | <span data-ttu-id="9c198-2032">\_PROGRAMFILESX86 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2032">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="9c198-2033">% SystemDrive% \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="9c198-2033">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="9c198-2034">\_Programma CSIDL \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="9c198-2034">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="9c198-2035">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2035">64 bit</span></span> | <span data-ttu-id="9c198-2036">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2036">64 bit</span></span> | <span data-ttu-id="9c198-2037">\_PROGRAMFILESX64 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2037">FOLDERID\_ProgramFilesX64</span></span> | <span data-ttu-id="9c198-2038">% File di programma% SystemDrive% \\</span><span class="sxs-lookup"><span data-stu-id="9c198-2038">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="9c198-2039">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-2039">None</span></span> |
| <span data-ttu-id="9c198-2040">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2040">64 bit</span></span> | <span data-ttu-id="9c198-2041">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2041">32 bit</span></span> | <span data-ttu-id="9c198-2042">\_Programmi FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2042">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="9c198-2043">% SystemDrive% \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="9c198-2043">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="9c198-2044">\_file di programma CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="9c198-2044">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="9c198-2045">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2045">64 bit</span></span> | <span data-ttu-id="9c198-2046">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2046">32 bit</span></span> | <span data-ttu-id="9c198-2047">\_PROGRAMFILESX86 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2047">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="9c198-2048">% SystemDrive% \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="9c198-2048">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="9c198-2049">\_Programma CSIDL \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="9c198-2049">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="9c198-2050">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2050">64 bit</span></span> | <span data-ttu-id="9c198-2051">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2051">32 bit</span></span> | <span data-ttu-id="9c198-2052">FOLDERID \_ ProgramFilesX64 (non supportato per le applicazioni a 32 bit)</span><span class="sxs-lookup"><span data-stu-id="9c198-2052">FOLDERID\_ProgramFilesX64 (not supported for 32-bit applications)</span></span> | <span data-ttu-id="9c198-2053">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-2053">Not applicable</span></span> | <span data-ttu-id="9c198-2054">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-2054">Not applicable</span></span> |


<span data-ttu-id="9c198-2055">**\_PROGRAMFILESCOMMON FOLDERID**</span><span class="sxs-lookup"><span data-stu-id="9c198-2055">**FOLDERID\_ProgramFilesCommon**</span></span>

| <span data-ttu-id="9c198-2056">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9c198-2056">Operating System</span></span> | <span data-ttu-id="9c198-2057">Applicazione</span><span class="sxs-lookup"><span data-stu-id="9c198-2057">Application</span></span> | <span data-ttu-id="9c198-2058">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2058">KNOWNFOLDERID</span></span> | <span data-ttu-id="9c198-2059">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-2059">Default Path</span></span> | <span data-ttu-id="9c198-2060">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-2060">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="9c198-2061">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2061">32 bit</span></span> | <span data-ttu-id="9c198-2062">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2062">32 bit</span></span> | <span data-ttu-id="9c198-2063">\_PROGRAMFILESCOMMON FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2063">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="9c198-2064">File comuni% ProgramFiles% \\</span><span class="sxs-lookup"><span data-stu-id="9c198-2064">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="9c198-2065">\_file di programma CSIDL \_ \_ comuni</span><span class="sxs-lookup"><span data-stu-id="9c198-2065">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="9c198-2066">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2066">32 bit</span></span> | <span data-ttu-id="9c198-2067">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2067">32 bit</span></span> | <span data-ttu-id="9c198-2068">\_PROGRAMFILESCOMMONX86 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2068">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="9c198-2069">File comuni% ProgramFiles% \\</span><span class="sxs-lookup"><span data-stu-id="9c198-2069">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="9c198-2070">\_File di programma CSIDL \_ \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="9c198-2070">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="9c198-2071">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2071">32 bit</span></span> | <span data-ttu-id="9c198-2072">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2072">32 bit</span></span> | <span data-ttu-id="9c198-2073">FOLDERID \_ ProgramFilesCommonX64 (undefined)</span><span class="sxs-lookup"><span data-stu-id="9c198-2073">FOLDERID\_ProgramFilesCommonX64 (undefined)</span></span> | <span data-ttu-id="9c198-2074">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-2074">Not applicable</span></span> | <span data-ttu-id="9c198-2075">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c198-2075">Not applicable</span></span> |
| <span data-ttu-id="9c198-2076">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2076">64 bit</span></span> | <span data-ttu-id="9c198-2077">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2077">64 bit</span></span> | <span data-ttu-id="9c198-2078">\_PROGRAMFILESCOMMON FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2078">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="9c198-2079">File comuni% ProgramFiles% \\</span><span class="sxs-lookup"><span data-stu-id="9c198-2079">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="9c198-2080">\_file di programma CSIDL \_ \_ comuni</span><span class="sxs-lookup"><span data-stu-id="9c198-2080">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="9c198-2081">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2081">64 bit</span></span> | <span data-ttu-id="9c198-2082">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2082">64 bit</span></span> | <span data-ttu-id="9c198-2083">\_PROGRAMFILESCOMMONX86 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2083">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="9c198-2084">% ProgramFiles (x86)% \\ file comuni</span><span class="sxs-lookup"><span data-stu-id="9c198-2084">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="9c198-2085">\_File di programma CSIDL \_ \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="9c198-2085">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="9c198-2086">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2086">64 bit</span></span> | <span data-ttu-id="9c198-2087">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2087">64 bit</span></span> | <span data-ttu-id="9c198-2088">\_PROGRAMFILESCOMMONX64 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2088">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="9c198-2089">File comuni% ProgramFiles% \\</span><span class="sxs-lookup"><span data-stu-id="9c198-2089">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="9c198-2090">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-2090">None</span></span> |
| <span data-ttu-id="9c198-2091">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2091">64 bit</span></span> | <span data-ttu-id="9c198-2092">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2092">32 bit</span></span> | <span data-ttu-id="9c198-2093">\_PROGRAMFILESCOMMON FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2093">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="9c198-2094">% ProgramFiles (x86)% \\ file comuni</span><span class="sxs-lookup"><span data-stu-id="9c198-2094">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="9c198-2095">\_file di programma CSIDL \_ \_ comuni</span><span class="sxs-lookup"><span data-stu-id="9c198-2095">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="9c198-2096">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2096">64 bit</span></span> | <span data-ttu-id="9c198-2097">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2097">32 bit</span></span> | <span data-ttu-id="9c198-2098">\_PROGRAMFILESCOMMONX86 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2098">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="9c198-2099">% ProgramFiles (x86)% \\ file comuni</span><span class="sxs-lookup"><span data-stu-id="9c198-2099">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="9c198-2100">\_File di programma CSIDL \_ \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="9c198-2100">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="9c198-2101">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2101">64 bit</span></span> | <span data-ttu-id="9c198-2102">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2102">32 bit</span></span> | <span data-ttu-id="9c198-2103">\_PROGRAMFILESCOMMONX64 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2103">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="9c198-2104">File comuni% ProgramFiles% \\</span><span class="sxs-lookup"><span data-stu-id="9c198-2104">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="9c198-2105">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c198-2105">None</span></span> |


<span data-ttu-id="9c198-2106">**\_Sistema FOLDERID**</span><span class="sxs-lookup"><span data-stu-id="9c198-2106">**FOLDERID\_System**</span></span>

| <span data-ttu-id="9c198-2107">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9c198-2107">Operating System</span></span> | <span data-ttu-id="9c198-2108">Applicazione</span><span class="sxs-lookup"><span data-stu-id="9c198-2108">Application</span></span> | <span data-ttu-id="9c198-2109">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2109">KNOWNFOLDERID</span></span> | <span data-ttu-id="9c198-2110">Predefinito Path</span><span class="sxs-lookup"><span data-stu-id="9c198-2110">Default Path</span></span> | <span data-ttu-id="9c198-2111">Equivalente CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-2111">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="9c198-2112">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2112">32 bit</span></span> | <span data-ttu-id="9c198-2113">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2113">32 bit</span></span> | <span data-ttu-id="9c198-2114">\_Sistema FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2114">FOLDERID\_System</span></span> | <span data-ttu-id="9c198-2115">% WINDIR% \\ system32</span><span class="sxs-lookup"><span data-stu-id="9c198-2115">%windir%\\system32</span></span> | <span data-ttu-id="9c198-2116">\_sistema CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-2116">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="9c198-2117">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2117">32 bit</span></span> | <span data-ttu-id="9c198-2118">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2118">32 bit</span></span> | <span data-ttu-id="9c198-2119">\_SYSTEMX86 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2119">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="9c198-2120">% WINDIR% \\ system32</span><span class="sxs-lookup"><span data-stu-id="9c198-2120">%windir%\\system32</span></span> | <span data-ttu-id="9c198-2121">\_SYSTEMX86 CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-2121">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="9c198-2122">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2122">64 bit</span></span> | <span data-ttu-id="9c198-2123">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2123">64 bit</span></span> | <span data-ttu-id="9c198-2124">\_Sistema FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2124">FOLDERID\_System</span></span> | <span data-ttu-id="9c198-2125">% WINDIR% \\ system32</span><span class="sxs-lookup"><span data-stu-id="9c198-2125">%windir%\\system32</span></span> | <span data-ttu-id="9c198-2126">\_sistema CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-2126">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="9c198-2127">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2127">64 bit</span></span> | <span data-ttu-id="9c198-2128">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2128">64 bit</span></span> | <span data-ttu-id="9c198-2129">\_SYSTEMX86 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2129">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="9c198-2130">% WINDIR% \\ SysWow64</span><span class="sxs-lookup"><span data-stu-id="9c198-2130">%windir%\\syswow64</span></span> | <span data-ttu-id="9c198-2131">\_SYSTEMX86 CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-2131">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="9c198-2132">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2132">64 bit</span></span> | <span data-ttu-id="9c198-2133">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2133">32 bit</span></span> | <span data-ttu-id="9c198-2134">\_Sistema FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2134">FOLDERID\_System</span></span> | <span data-ttu-id="9c198-2135">% WINDIR% \\ system32</span><span class="sxs-lookup"><span data-stu-id="9c198-2135">%windir%\\system32</span></span> | <span data-ttu-id="9c198-2136">\_sistema CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-2136">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="9c198-2137">64 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2137">64 bit</span></span> | <span data-ttu-id="9c198-2138">32 bit</span><span class="sxs-lookup"><span data-stu-id="9c198-2138">32 bit</span></span> | <span data-ttu-id="9c198-2139">\_SYSTEMX86 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9c198-2139">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="9c198-2140">% WINDIR% \\ SysWow64</span><span class="sxs-lookup"><span data-stu-id="9c198-2140">%windir%\\syswow64</span></span> | <span data-ttu-id="9c198-2141">\_SYSTEMX86 CSIDL</span><span class="sxs-lookup"><span data-stu-id="9c198-2141">CSIDL\_SYSTEMX86</span></span> |


<span data-ttu-id="9c198-2142">Sono state usate stringhe di ambiente per fornire percorsi generici in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="9c198-2142">We have used environment strings to provide generic paths throughout this topic.</span></span> <span data-ttu-id="9c198-2143">Le tabelle seguenti forniscono esempi dei percorsi rappresentati da tali stringhe di ambiente.</span><span class="sxs-lookup"><span data-stu-id="9c198-2143">The following tables give examples of the paths those environment strings represent.</span></span> <span data-ttu-id="9c198-2144">In alcuni casi, questi percorsi potrebbero non corrispondere a quelli di un determinato computer a causa di scelte effettuate durante l'installazione o il reindirizzamento delle cartelle successivo.</span><span class="sxs-lookup"><span data-stu-id="9c198-2144">In some cases, these paths might not match those on a particular computer because of choices made during installation or later folder redirection.</span></span> <span data-ttu-id="9c198-2145">Si noti che alcuni percorsi sono stati modificati per Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9c198-2145">Note that some paths have changed for Windows Vista.</span></span>


<span data-ttu-id="9c198-2146">**Windows Vista e versioni successive**</span><span class="sxs-lookup"><span data-stu-id="9c198-2146">**Windows Vista and later**</span></span>

| <span data-ttu-id="9c198-2147">Stringa di ambiente</span><span class="sxs-lookup"><span data-stu-id="9c198-2147">Environment String</span></span> | <span data-ttu-id="9c198-2148">Percorso di esempio</span><span class="sxs-lookup"><span data-stu-id="9c198-2148">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="9c198-2149">ALLUSERSPROFILE</span><span class="sxs-lookup"><span data-stu-id="9c198-2149">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="9c198-2150">C: \\ ProgramData</span><span class="sxs-lookup"><span data-stu-id="9c198-2150">C:\\ProgramData</span></span> |
| <span data-ttu-id="9c198-2151">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="9c198-2151">%APPDATA%</span></span> | <span data-ttu-id="9c198-2152">C: \\ utenti \\ *nomeutente* \\ AppData \\ roaming</span><span class="sxs-lookup"><span data-stu-id="9c198-2152">C:\\Users\\*username*\\AppData\\Roaming</span></span> |
| <span data-ttu-id="9c198-2153">LocalAppData</span><span class="sxs-lookup"><span data-stu-id="9c198-2153">%LOCALAPPDATA%</span></span> | <span data-ttu-id="9c198-2154">C: \\ utenti \\ *nomeutente* \\ AppData \\ locale</span><span class="sxs-lookup"><span data-stu-id="9c198-2154">C:\\Users\\*username*\\AppData\\Local</span></span> |
| <span data-ttu-id="9c198-2155">%ProgramData%</span><span class="sxs-lookup"><span data-stu-id="9c198-2155">%ProgramData%</span></span> | <span data-ttu-id="9c198-2156">C: \\ ProgramData</span><span class="sxs-lookup"><span data-stu-id="9c198-2156">C:\\ProgramData</span></span> |
| <span data-ttu-id="9c198-2157">%ProgramFiles%</span><span class="sxs-lookup"><span data-stu-id="9c198-2157">%ProgramFiles%</span></span> | <span data-ttu-id="9c198-2158">C: \\ programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-2158">C:\\Program Files</span></span> |
| <span data-ttu-id="9c198-2159">%ProgramFiles(x86)%</span><span class="sxs-lookup"><span data-stu-id="9c198-2159">%ProgramFiles(x86)%</span></span> | <span data-ttu-id="9c198-2160">C: \\ programmi (x86)</span><span class="sxs-lookup"><span data-stu-id="9c198-2160">C:\\Program Files (x86)</span></span> |
| <span data-ttu-id="9c198-2161">PUBBLICO</span><span class="sxs-lookup"><span data-stu-id="9c198-2161">%PUBLIC%</span></span> | <span data-ttu-id="9c198-2162">C: \\ utenti \\ pubblici</span><span class="sxs-lookup"><span data-stu-id="9c198-2162">C:\\Users\\Public</span></span> |
| <span data-ttu-id="9c198-2163">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="9c198-2163">%SystemDrive%</span></span> | <span data-ttu-id="9c198-2164">C:</span><span class="sxs-lookup"><span data-stu-id="9c198-2164">C:</span></span> |
| <span data-ttu-id="9c198-2165">UserProfile</span><span class="sxs-lookup"><span data-stu-id="9c198-2165">%USERPROFILE%</span></span> | <span data-ttu-id="9c198-2166">C: \\ \\ *nome utente* utenti</span><span class="sxs-lookup"><span data-stu-id="9c198-2166">C:\\Users\\*username*</span></span> |
| <span data-ttu-id="9c198-2167">WINDIR</span><span class="sxs-lookup"><span data-stu-id="9c198-2167">%windir%</span></span> | <span data-ttu-id="9c198-2168">C: \\ Windows</span><span class="sxs-lookup"><span data-stu-id="9c198-2168">C:\\Windows</span></span> |


<span data-ttu-id="9c198-2169">**Windows XP e versioni precedenti**</span><span class="sxs-lookup"><span data-stu-id="9c198-2169">**Windows XP and earlier**</span></span>

| <span data-ttu-id="9c198-2170">Stringa di ambiente</span><span class="sxs-lookup"><span data-stu-id="9c198-2170">Environment String</span></span> | <span data-ttu-id="9c198-2171">Percorso di esempio</span><span class="sxs-lookup"><span data-stu-id="9c198-2171">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="9c198-2172">ALLUSERSPROFILE</span><span class="sxs-lookup"><span data-stu-id="9c198-2172">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="9c198-2173">C: \\ Documents and Settings \\ All Users</span><span class="sxs-lookup"><span data-stu-id="9c198-2173">C:\\Documents and Settings\\All Users</span></span> |
| <span data-ttu-id="9c198-2174">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="9c198-2174">%APPDATA%</span></span> | <span data-ttu-id="9c198-2175">C: \\ Documents and Settings \\ *nome utente* \\ dati applicazione</span><span class="sxs-lookup"><span data-stu-id="9c198-2175">C:\\Documents and Settings\\*username*\\Application Data</span></span> |
| <span data-ttu-id="9c198-2176">%ProgramFiles%</span><span class="sxs-lookup"><span data-stu-id="9c198-2176">%ProgramFiles%</span></span> | <span data-ttu-id="9c198-2177">C: \\ programmi</span><span class="sxs-lookup"><span data-stu-id="9c198-2177">C:\\Program Files</span></span> |
| <span data-ttu-id="9c198-2178">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="9c198-2178">%SystemDrive%</span></span> | <span data-ttu-id="9c198-2179">C:</span><span class="sxs-lookup"><span data-stu-id="9c198-2179">C:</span></span> |
| <span data-ttu-id="9c198-2180">UserProfile</span><span class="sxs-lookup"><span data-stu-id="9c198-2180">%USERPROFILE%</span></span> | <span data-ttu-id="9c198-2181">C: \\ Documents and Settings \\ *nome utente*</span><span class="sxs-lookup"><span data-stu-id="9c198-2181">C:\\Documents and Settings\\*username*</span></span> |
| <span data-ttu-id="9c198-2182">WINDIR</span><span class="sxs-lookup"><span data-stu-id="9c198-2182">%windir%</span></span> | <span data-ttu-id="9c198-2183">C: \\ Windows</span><span class="sxs-lookup"><span data-stu-id="9c198-2183">C:\\Windows</span></span> |


## <a name="requirements"></a><span data-ttu-id="9c198-2184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c198-2184">Requirements</span></span>


| <span data-ttu-id="9c198-2185">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c198-2185">Requirement</span></span> | <span data-ttu-id="9c198-2186">Valore</span><span class="sxs-lookup"><span data-stu-id="9c198-2186">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c198-2187">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c198-2187">Header</span></span><br/> | <dl> <span data-ttu-id="9c198-2188"><dt>KnownFolders. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c198-2188"><dt>Knownfolders.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c198-2189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c198-2189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c198-2190">**CSIDL**</span><span class="sxs-lookup"><span data-stu-id="9c198-2190">**CSIDL**</span></span>](csidl.md)
</dt> <dt>

[<span data-ttu-id="9c198-2191">Cartelle note</span><span class="sxs-lookup"><span data-stu-id="9c198-2191">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="9c198-2192">Utilizzo di cartelle note nelle applicazioni</span><span class="sxs-lookup"><span data-stu-id="9c198-2192">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
</dt> <dt>

[<span data-ttu-id="9c198-2193">Come estendere le cartelle note con cartelle personalizzate</span><span class="sxs-lookup"><span data-stu-id="9c198-2193">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
</dt> <dt>

<span data-ttu-id="9c198-2194">[Esempio di cartelle note](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9c198-2194">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
