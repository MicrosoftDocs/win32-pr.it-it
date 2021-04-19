---
description: Contiene gli attributi di condivisione DDE gestiti da NetDDE Share database Manager (DSDM).
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: Struttura NDDESHAREINFO (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 975382272a4e2c7cc56b0ddf593905b4d745a48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317315"
---
# <a name="nddeshareinfo-structure"></a><span data-ttu-id="78211-103">Struttura NDDESHAREINFO</span><span class="sxs-lookup"><span data-stu-id="78211-103">NDDESHAREINFO structure</span></span>

<span data-ttu-id="78211-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="78211-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="78211-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="78211-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="78211-106">Contiene gli attributi di condivisione DDE gestiti da NetDDE Share database Manager (DSDM).</span><span class="sxs-lookup"><span data-stu-id="78211-106">Contains DDE share attributes maintained by the NetDDE Share Database Manager (DSDM).</span></span> <span data-ttu-id="78211-107">Il descrittore di sicurezza associato a ogni condivisione DDE non viene passato tramite questa struttura, ma è possibile accedervi tramite funzioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="78211-107">The security descriptor associated with each DDE share is not passed through this structure but is accessed through specific functions.</span></span> <span data-ttu-id="78211-108">L'API DSDM di NetDDE accetta questa struttura per le funzioni set; per le funzioni Get, DSDM restituisce la struttura compressa nel buffer fornito insieme ai dati a cui fanno riferimento i membri **lpszShareName**, **lpszAppTopicList** e **lpszItemList**.</span><span class="sxs-lookup"><span data-stu-id="78211-108">The NetDDE DSDM API accepts this structure for set functions; for get functions, the DSDM returns the structure packed into the supplied buffer along with the data referenced by the members **lpszShareName**, **lpszAppTopicList**, and **lpszItemList**.</span></span>

## <a name="syntax"></a><span data-ttu-id="78211-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78211-109">Syntax</span></span>


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a><span data-ttu-id="78211-110">Members</span><span class="sxs-lookup"><span data-stu-id="78211-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="78211-111">**lRevision**</span><span class="sxs-lookup"><span data-stu-id="78211-111">**lRevision**</span></span>
</dt> <dd>

<span data-ttu-id="78211-112">Livello di revisione della struttura **NDDESHAREINFO** .</span><span class="sxs-lookup"><span data-stu-id="78211-112">The revision level of the **NDDESHAREINFO** structure.</span></span> <span data-ttu-id="78211-113">Attualmente, il livello di revisione è 1.</span><span class="sxs-lookup"><span data-stu-id="78211-113">Currently, the revision level is 1.</span></span>

</dd> <dt>

<span data-ttu-id="78211-114">**lpszShareName**</span><span class="sxs-lookup"><span data-stu-id="78211-114">**lpszShareName**</span></span>
</dt> <dd>

<span data-ttu-id="78211-115">Nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="78211-115">The name of the share.</span></span> <span data-ttu-id="78211-116">La lunghezza della stringa non deve superare il numero massimo di \_ caratteri NDDESHARENAME.</span><span class="sxs-lookup"><span data-stu-id="78211-116">This string must be no more than MAX\_NDDESHARENAME characters long.</span></span>

</dd> <dt>

<span data-ttu-id="78211-117">**lShareType**</span><span class="sxs-lookup"><span data-stu-id="78211-117">**lShareType**</span></span>
</dt> <dd>

<span data-ttu-id="78211-118">Uno o più tipi di condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="78211-118">One or more DDE share types.</span></span> <span data-ttu-id="78211-119">Questo membro può essere una combinazione dei seguenti tipi di condivisione DDE supportati.</span><span class="sxs-lookup"><span data-stu-id="78211-119">This member can be a combination of the following supported DDE share types.</span></span>



| <span data-ttu-id="78211-120">Tipo di condivisione</span><span class="sxs-lookup"><span data-stu-id="78211-120">Share type</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="78211-121">Significato</span><span class="sxs-lookup"><span data-stu-id="78211-121">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <span data-ttu-id="78211-122"><dt>**Condividi \_ Digitare \_ New**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="78211-122"><dt>**SHARE\_TYPE\_NEW**</dt> <dt>0x02</dt></span></span> </dl>          | <span data-ttu-id="78211-123">La condivisione contiene una coppia applicazione/argomento OLE.</span><span class="sxs-lookup"><span data-stu-id="78211-123">The share contains an OLE application/topic pair.</span></span><br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <span data-ttu-id="78211-124"><dt>**Condividi \_ Digitare \_**</dt> <dt>0x01</dt> precedente</span><span class="sxs-lookup"><span data-stu-id="78211-124"><dt>**SHARE\_TYPE\_OLD**</dt> <dt>0x01</dt></span></span> </dl>          | <span data-ttu-id="78211-125">La condivisione contiene una coppia applicazione/argomento DDE.</span><span class="sxs-lookup"><span data-stu-id="78211-125">The share contains a DDE application/topic pair.</span></span><br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <span data-ttu-id="78211-126"><dt>**Condividi \_ Digitare \_**</dt> <dt>0x04</dt> statico</span><span class="sxs-lookup"><span data-stu-id="78211-126"><dt>**SHARE\_TYPE\_STATIC**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="78211-127">La condivisione contiene una coppia applicazione/argomento statica.</span><span class="sxs-lookup"><span data-stu-id="78211-127">The share contains a static application/topic pair.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="78211-128">**lpszAppTopicList**</span><span class="sxs-lookup"><span data-stu-id="78211-128">**lpszAppTopicList**</span></span>
</dt> <dd>

<span data-ttu-id="78211-129">Puntatore a un buffer contenente stringhe con terminazione null per le coppie di applicazione/argomento DDE, OLE e statiche.</span><span class="sxs-lookup"><span data-stu-id="78211-129">A pointer to a buffer containing null-terminated strings for the DDE, OLE, and static application/topic pairs.</span></span> <span data-ttu-id="78211-130">Il buffer deve avere il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="78211-130">The buffer should be in the following format:</span></span>

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

<span data-ttu-id="78211-131">**fSharedFlag**</span><span class="sxs-lookup"><span data-stu-id="78211-131">**fSharedFlag**</span></span>
</dt> <dd>

<span data-ttu-id="78211-132">Se questo membro è **false**, la condivisione DDE non consentirà agli utenti remoti di comunicare tramite DDE tramite DDE.</span><span class="sxs-lookup"><span data-stu-id="78211-132">If this member is **FALSE**, the DDE share will not allow remote users to communicate through it by using DDE.</span></span> <span data-ttu-id="78211-133">Tuttavia, gli utenti locali possono comunque comunicare tramite la condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="78211-133">However, local users can still communicate through the DDE share.</span></span> <span data-ttu-id="78211-134">I collegamenti client locali sono sempre impliciti se l'elenco DACL associato concede l'accesso.</span><span class="sxs-lookup"><span data-stu-id="78211-134">Local client links are always implied if the associated DACL grants access.</span></span>

</dd> <dt>

<span data-ttu-id="78211-135">**fService**</span><span class="sxs-lookup"><span data-stu-id="78211-135">**fService**</span></span>
</dt> <dd>

<span data-ttu-id="78211-136">Se questo membro è impostato, la condivisione DDE non verificherà se l'utente corrente lo ha impostato come attendibile prima di consentire la comunicazione DDE.</span><span class="sxs-lookup"><span data-stu-id="78211-136">If this member is set, the DDE share will not check whether the current user has set it as trusted before allowing DDE communication.</span></span>

</dd> <dt>

<span data-ttu-id="78211-137">**fStartAppFlag**</span><span class="sxs-lookup"><span data-stu-id="78211-137">**fStartAppFlag**</span></span>
</dt> <dd>

<span data-ttu-id="78211-138">Se questo membro è impostato e la condivisione è attendibile per avviare le applicazioni, NetDDE tenterà di avviare l'applicazione specificata da **lpszAppTopicList** se non è possibile avviare inizialmente una conversazione DDE con l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="78211-138">If this member is set and the share is trusted to start applications, NetDDE will attempt to start the application specified by **lpszAppTopicList** if it cannot initially start a DDE conversation with the application.</span></span>

</dd> <dt>

<span data-ttu-id="78211-139">**nCmdShow**</span><span class="sxs-lookup"><span data-stu-id="78211-139">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="78211-140">Quando NetDDE avvia un'applicazione per avviare una conversazione DDE, questo valore viene inviato all'applicazione tramite il parametro *nCmdShow* della funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="78211-140">When NetDDE starts an application to initiate a DDE conversation, this value is sent to the application through the *nCmdShow* parameter of the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="78211-141">Definisce la modalità preferita per la finestra dell'applicazione da visualizzare in.</span><span class="sxs-lookup"><span data-stu-id="78211-141">It defines the preferred mode for the application window to be shown in.</span></span> <span data-ttu-id="78211-142">Questo parametro è significativo solo se **fStartAppFlag** è attivo.</span><span class="sxs-lookup"><span data-stu-id="78211-142">This parameter is significant only if **fStartAppFlag** is active.</span></span> <span data-ttu-id="78211-143">L'utente connesso nel cui contesto viene avviata l'applicazione può anche eseguire l'override di questa opzione quando si innalza di livello la condivisione allo stato attendibile.</span><span class="sxs-lookup"><span data-stu-id="78211-143">The logged on user in whose context the application is started can also override this option when promoting the share to trusted status.</span></span> <span data-ttu-id="78211-144">Il valore predefinito per questo membro è SW \_ SHOWMAXIMIZED.</span><span class="sxs-lookup"><span data-stu-id="78211-144">The default for this member is SW\_SHOWMAXIMIZED.</span></span>

</dd> <dt>

<span data-ttu-id="78211-145">**qModifyId**</span><span class="sxs-lookup"><span data-stu-id="78211-145">**qModifyId**</span></span>
</dt> <dd>

<span data-ttu-id="78211-146">Numero di serie a 8 byte che indica il numero di serie della modifica della condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="78211-146">An 8-byte serial number that indicates the modification serial number of the DDE share.</span></span> <span data-ttu-id="78211-147">Ogni volta che la condivisione DDE viene modificata da una chiamata a [**NDdeShareSetInfo**](nddesharesetinfo.md) o [**NDdeSetShareSecurity**](nddesetsharesecurity.md) , questi valori vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="78211-147">Every time the DDE share is modified by a [**NDdeShareSetInfo**](nddesharesetinfo.md) or [**NDdeSetShareSecurity**](nddesetsharesecurity.md) call, these values are changed.</span></span>

</dd> <dt>

<span data-ttu-id="78211-148">**cNumItems**</span><span class="sxs-lookup"><span data-stu-id="78211-148">**cNumItems**</span></span>
</dt> <dd>

<span data-ttu-id="78211-149">Numero di elementi elencati in **lpszItemList**.</span><span class="sxs-lookup"><span data-stu-id="78211-149">The number of items listed in **lpszItemList**.</span></span> <span data-ttu-id="78211-150">Se **cNumItems** è zero, **lpszItemList** è vuoto e le informazioni sulla condivisione e il descrittore di sicurezza associato si applicano a tutti gli elementi serviti dall'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="78211-150">If **cNumItems** is zero, then **lpszItemList** is empty, and the share information and associated security descriptor apply to all items serviced by the associated application.</span></span>

</dd> <dt>

<span data-ttu-id="78211-151">**lpszItemList**</span><span class="sxs-lookup"><span data-stu-id="78211-151">**lpszItemList**</span></span>
</dt> <dd>

<span data-ttu-id="78211-152">Puntatore a un buffer contenente stringhe con terminazione null che specificano gli elementi in cui l'applicazione client in una transazione DDE può richiedere o avviare i cicli di notifica.</span><span class="sxs-lookup"><span data-stu-id="78211-152">A pointer to a buffer containing null-terminated strings that specify the items the client application in a DDE transaction can request or start advise loops on.</span></span> <span data-ttu-id="78211-153">Se non sono elencati elementi, la condivisione DDE consente l'utilizzo di qualsiasi elemento.</span><span class="sxs-lookup"><span data-stu-id="78211-153">If no items are listed, the DDE share allows any item to be used.</span></span> <span data-ttu-id="78211-154">Il numero di elementi nell'elenco deve corrispondere al numero di **cNumItems** .</span><span class="sxs-lookup"><span data-stu-id="78211-154">The number of items in the list must match the **cNumItems** count.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78211-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78211-155">Requirements</span></span>



| <span data-ttu-id="78211-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="78211-156">Requirement</span></span> | <span data-ttu-id="78211-157">Valore</span><span class="sxs-lookup"><span data-stu-id="78211-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="78211-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78211-158">Minimum supported client</span></span><br/> | <span data-ttu-id="78211-159">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="78211-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="78211-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78211-160">Minimum supported server</span></span><br/> | <span data-ttu-id="78211-161">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="78211-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="78211-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78211-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="78211-163"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="78211-163"><dt>Nddeapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78211-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78211-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78211-165">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="78211-165">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="78211-166">Strutture DDE di rete</span><span class="sxs-lookup"><span data-stu-id="78211-166">Network DDE Structures</span></span>](network-dde-structures.md)
</dt> <dt>

[<span data-ttu-id="78211-167">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="78211-167">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> <dt>

[<span data-ttu-id="78211-168">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="78211-168">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> <dt>

[<span data-ttu-id="78211-169">**WinMain**</span><span class="sxs-lookup"><span data-stu-id="78211-169">**WinMain**</span></span>](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

