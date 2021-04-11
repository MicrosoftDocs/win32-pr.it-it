---
description: DDE di rete fornisce funzioni che consentono di eliminare una condivisione, ottenere o impostare le informazioni di condivisione o enumerare le condivisioni.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Gestione delle condivisioni DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350951"
---
# <a name="managing-dde-shares"></a><span data-ttu-id="314da-103">Gestione delle condivisioni DDE</span><span class="sxs-lookup"><span data-stu-id="314da-103">Managing DDE Shares</span></span>

<span data-ttu-id="314da-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="314da-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="314da-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="314da-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="314da-106">DDE di rete fornisce funzioni che consentono di eliminare una condivisione, ottenere o impostare le informazioni di condivisione o enumerare le condivisioni.</span><span class="sxs-lookup"><span data-stu-id="314da-106">Network DDE provides functions that allow you to delete a share, get or set share information, or enumerate shares.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="314da-107">Attività</span><span class="sxs-lookup"><span data-stu-id="314da-107">Task</span></span></th>
<th><span data-ttu-id="314da-108">Procedura</span><span class="sxs-lookup"><span data-stu-id="314da-108">Procedure</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="314da-109">Eliminare una condivisione DDE</span><span class="sxs-lookup"><span data-stu-id="314da-109">Delete a DDE share</span></span></td>
<td><span data-ttu-id="314da-110">Usare la funzione <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="314da-110">Use the <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="314da-111">Ottenere informazioni sulla condivisione DDE</span><span class="sxs-lookup"><span data-stu-id="314da-111">Get DDE share information</span></span></td>
<td><span data-ttu-id="314da-112">Usare la funzione <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="314da-112">Use the <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="314da-113">Impostare le informazioni sulla condivisione DDE</span><span class="sxs-lookup"><span data-stu-id="314da-113">Set DDE share information</span></span></td>
<td><span data-ttu-id="314da-114">Usare la funzione <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="314da-114">Use the <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="314da-115">Enumera condivisioni DDE</span><span class="sxs-lookup"><span data-stu-id="314da-115">Enumerate DDE shares</span></span></td>
<td><span data-ttu-id="314da-116">Usare la funzione <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="314da-116">Use the <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> function.</span></span> <span data-ttu-id="314da-117">È inoltre possibile enumerare le condivisioni DDE attendibili tramite la funzione <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="314da-117">You can also enumerate the trusted DDE shares by using the <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="314da-118">Enumerazione degli utenti connessi</span><span class="sxs-lookup"><span data-stu-id="314da-118">Enumerate connected users</span></span></td>
<td><span data-ttu-id="314da-119">Usare la funzione <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="314da-119">Use the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="314da-120">Modificare il nome della condivisione DDE</span><span class="sxs-lookup"><span data-stu-id="314da-120">Change the DDE share name</span></span></td>
<td><span data-ttu-id="314da-121">Eliminare la condivisione precedente e creare una nuova condivisione.</span><span class="sxs-lookup"><span data-stu-id="314da-121">Delete the old share and create a new share.</span></span>
<ol>
<li><span data-ttu-id="314da-122">Recuperare le informazioni sulla condivisione utilizzando <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="314da-122">Retrieve the share information using <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="314da-123">Rimuovere la condivisione usando <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="314da-123">Remove the share using <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</span></span></li>
<li><span data-ttu-id="314da-124">Modificare il membro <strong>lpszShareName</strong> della struttura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> restituita da <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="314da-124">Change the <strong>lpszShareName</strong> member of the <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure returned by <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="314da-125">Passare la struttura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> modificata a <a href="nddeshareadd.md"><strong>NDDEShareAdd</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="314da-125">Pass the modified <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure to <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

