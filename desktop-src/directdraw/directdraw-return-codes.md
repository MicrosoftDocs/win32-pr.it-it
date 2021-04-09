---
title: Codici restituiti di DirectDraw (ddraw. h)
description: Gli errori sono rappresentati da valori negativi e non possono essere combinati.
ms.assetid: F713193E-3614-4741-B293-D312C170270A
topic_type:
- apiref
api_name:
- DD_OK
- DDERR_ALREADYINITIALIZED
- DDERR_BLTFASTCANTCLIP
- DDERR_CANNOTATTACHSURFACE
- DDERR_CANNOTDETACHSURFACE
- DDERR_CANTCREATEDC
- DDERR_CANTDUPLICATE
- DDERR_CANTLOCKSURFACE
- DDERR_CANTPAGELOCK
- DDERR_CANTPAGEUNLOCK
- DDERR_CLIPPERISUSINGHWND
- DDERR_COLORKEYNOTSET
- DDERR_CURRENTLYNOTAVAIL
- DDERR_DDSCAPSCOMPLEXREQUIRED
- DDERR_DCALREADYCREATED
- DDERR_DEVICEDOESNTOWNSURFACE
- DDERR_DIRECTDRAWALREADYCREATED
- DDERR_EXCEPTION
- DDERR_EXCLUSIVEMODEALREADYSET
- DDERR_EXPIRED
- DDERR_GENERIC
- DDERR_HEIGHTALIGN
- DDERR_HWNDALREADYSET
- DDERR_HWNDSUBCLASSED
- DDERR_IMPLICITLYCREATED
- DDERR_INCOMPATIBLEPRIMARY
- DDERR_INVALIDCAPS
- DDERR_INVALIDCLIPLIST
- DDERR_INVALIDDIRECTDRAWGUID
- DDERR_INVALIDMODE
- DDERR_INVALIDOBJECT
- DDERR_INVALIDPARAMS
- DDERR_INVALIDPIXELFORMAT
- DDERR_INVALIDPOSITION
- DDERR_INVALIDRECT
- DDERR_INVALIDSTREAM
- DDERR_INVALIDSURFACETYPE
- DDERR_LOCKEDSURFACES
- DDERR_MOREDATA
- DDERR_NEWMODE
- DDERR_NO3D
- DDERR_NOALPHAHW
- DDERR_NOBLTHW
- DDERR_NOCLIPLIST
- DDERR_NOCLIPPERATTACHED
- DDERR_NOCOLORCONVHW
- DDERR_NOCOLORKEY
- DDERR_NOCOLORKEYHW
- DDERR_NOCOOPERATIVELEVELSET
- DDERR_NODC
- DDERR_NODDROPSHW
- DDERR_NODIRECTDRAWHW
- DDERR_NODIRECTDRAWSUPPORT
- DDERR_NODRIVERSUPPORT
- DDERR_NOEMULATION
- DDERR_NOEXCLUSIVEMODE
- DDERR_NOFLIPHW
- DDERR_NOFOCUSWINDOW
- DDERR_NOGDI
- DDERR_NOHWND
- DDERR_NOMIPMAPHW
- DDERR_NOMIRRORHW
- DDERR_NOMONITORINFORMATION
- DDERR_NONONLOCALVIDMEM
- DDERR_NOOPTIMIZEHW
- DDERR_NOOVERLAYDEST
- DDERR_NOOVERLAYHW
- DDERR_NOPALETTEATTACHED
- DDERR_NOPALETTEHW
- DDERR_NORASTEROPHW
- DDERR_NOROTATIONHW
- DDERR_NOSTEREOHARDWARE
- DDERR_NOSTRETCHHW
- DDERR_NOSURFACELEFT
- DDERR_NOT4BITCOLOR
- DDERR_NOT4BITCOLORINDEX
- DDERR_NOT8BITCOLOR
- DDERR_NOTAOVERLAYSURFACE
- DDERR_NOTEXTUREHW
- DDERR_NOTFLIPPABLE
- DDERR_NOTFOUND
- DDERR_NOTINITIALIZED
- DDERR_NOTLOADED
- DDERR_NOTLOCKED
- DDERR_NOTPAGELOCKED
- DDERR_NOTPALETTIZED
- DDERR_NOVSYNCHW
- DDERR_NOZBUFFERHW
- DDERR_NOZOVERLAYHW
- DDERR_OUTOFCAPS
- DDERR_OUTOFMEMORY
- DDERR_OUTOFVIDEOMEMORY
- DDERR_OVERLAPPINGRECTS
- DDERR_OVERLAYCANTCLIP
- DDERR_OVERLAYCOLORKEYONLYONEACTIVE
- DDERR_OVERLAYNOTVISIBLE
- DDERR_PALETTEBUSY
- DDERR_PRIMARYSURFACEALREADYEXISTS
- DDERR_REGIONTOOSMALL
- DDERR_SURFACEALREADYATTACHED
- DDERR_SURFACEALREADYDEPENDENT
- DDERR_SURFACEBUSY
- DDERR_SURFACEISOBSCURED
- DDERR_SURFACELOST
- DDERR_SURFACENOTATTACHED
- DDERR_TESTFINISHED
- DDERR_TOOBIGHEIGHT
- DDERR_TOOBIGSIZE
- DDERR_TOOBIGWIDTH
- DDERR_UNSUPPORTED
- DDERR_UNSUPPORTEDFORMAT
- DDERR_UNSUPPORTEDMASK
- DDERR_UNSUPPORTEDMODE
- DDERR_VERTICALBLANKINPROGRESS
- DDERR_VIDEONOTACTIVE
- DDERR_WASSTILLDRAWING
- DDERR_WRONGMODE
- DDERR_XALIGN
api_location:
- Ddraw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70ff2003edc382bac2823235f01f58ffea0d91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886305"
---
# <a name="directdraw-return-codes"></a><span data-ttu-id="ea142-103">Codici restituiti di DirectDraw</span><span class="sxs-lookup"><span data-stu-id="ea142-103">DirectDraw Return Codes</span></span>

<span data-ttu-id="ea142-104">Gli errori sono rappresentati da valori negativi e non possono essere combinati.</span><span class="sxs-lookup"><span data-stu-id="ea142-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="ea142-105">In questa tabella sono elencati i valori che possono essere restituiti da tutti i metodi delle [interfacce DirectDraw](directdraw-interfaces.md) e delle [funzioni DirectDraw](directdraw-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ea142-105">This table lists the values that can be returned by all methods of the [DirectDraw Interfaces](directdraw-interfaces.md) and [DirectDraw Functions](directdraw-functions.md).</span></span> <span data-ttu-id="ea142-106">Per un elenco dei codici di errore che possono essere restituiti da ogni metodo o funzione, vedere la descrizione del metodo o della funzione.</span><span class="sxs-lookup"><span data-stu-id="ea142-106">For a list of the error codes that each method or function can return, see the method or function description.</span></span>

<dl> <dt>

<span data-ttu-id="ea142-107"><span id="DD_OK"></span><span id="dd_ok"></span>**DD \_ OK**</span><span class="sxs-lookup"><span data-stu-id="ea142-107"><span id="DD_OK"></span><span id="dd_ok"></span>**DD\_OK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-108">La richiesta è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="ea142-108">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-109"><span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**\_ALREADYINITIALIZED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-109"><span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR\_ALREADYINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-110">L'oggetto è già stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="ea142-110">The object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-111"><span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**\_BLTFASTCANTCLIP DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-111"><span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR\_BLTFASTCANTCLIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-112">Un oggetto DirectDrawClipper è associato a una superficie di origine che è passata a una chiamata al metodo [**IDirectDrawSurface7:: BltFast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) .</span><span class="sxs-lookup"><span data-stu-id="ea142-112">A DirectDrawClipper object is attached to a source surface that has passed into a call to the [**IDirectDrawSurface7::BltFast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-113"><span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**\_CANNOTATTACHSURFACE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-113"><span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR\_CANNOTATTACHSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-114">Non è possibile collegare una superficie a un'altra superficie richiesta.</span><span class="sxs-lookup"><span data-stu-id="ea142-114">A surface cannot be attached to another requested surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-115"><span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**\_CANNOTDETACHSURFACE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-115"><span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR\_CANNOTDETACHSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-116">Non è possibile scollegare una superficie da un'altra superficie richiesta.</span><span class="sxs-lookup"><span data-stu-id="ea142-116">A surface cannot be detached from another requested surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-117"><span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**\_CANTCREATEDC DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-117"><span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR\_CANTCREATEDC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-118">Windows non è in grado di creare altri contesti di dispositivo o un controller di dominio ha richiesto una superficie indicizzata della tavolozza quando la superficie non aveva una tavolozza e la modalità di visualizzazione non è stata indicizzata (in questo caso, DirectDraw non è in grado di selezionare una tavolozza appropriata nel controller di dominio).</span><span class="sxs-lookup"><span data-stu-id="ea142-118">Windows cannot create any more device contexts (DCs), or a DC has requested a palette-indexed surface when the surface had no palette and the display mode was not palette-indexed (in this case, DirectDraw cannot select a proper palette into the DC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-119"><span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**\_CANTDUPLICATE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-119"><span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR\_CANTDUPLICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-120">Non è possibile duplicare le superfici primarie e 3D, o le superfici create in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="ea142-120">Primary and 3-D surfaces, or surfaces that are implicitly created, cannot be duplicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-121"><span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**\_CANTLOCKSURFACE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-121"><span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR\_CANTLOCKSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-122">L'accesso a questa superficie è stato rifiutato perché è stato effettuato un tentativo di bloccare la superficie primaria senza il supporto per l'interfaccia di controllo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea142-122">Access to this surface is refused because an attempt was made to lock the primary surface without Display Control Interface (DCI) support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-123"><span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**\_CANTPAGELOCK DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-123"><span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR\_CANTPAGELOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-124">Tentativo di blocco di una superficie di pagina non riuscito.</span><span class="sxs-lookup"><span data-stu-id="ea142-124">An attempt to page-lock a surface failed.</span></span> <span data-ttu-id="ea142-125">Il blocco di pagina non funziona in una superficie di memoria di visualizzazione o in una superficie primaria emulata.</span><span class="sxs-lookup"><span data-stu-id="ea142-125">Page lock does not work on a display-memory surface or an emulated primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-126"><span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**\_CANTPAGEUNLOCK DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-126"><span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR\_CANTPAGEUNLOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-127">Tentativo di sblocco di una superficie non riuscito.</span><span class="sxs-lookup"><span data-stu-id="ea142-127">An attempt to page-unlock a surface failed.</span></span> <span data-ttu-id="ea142-128">Lo sblocco della pagina non funziona in una superficie di memoria di visualizzazione o in una superficie primaria emulata.</span><span class="sxs-lookup"><span data-stu-id="ea142-128">Page unlock does not work on a display-memory surface or an emulated primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-129"><span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**\_CLIPPERISUSINGHWND DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-129"><span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR\_CLIPPERISUSINGHWND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-130">È stato effettuato un tentativo di impostare un elenco di clip per un oggetto DirectDrawClipper che sta già monitorando un handle di finestra.</span><span class="sxs-lookup"><span data-stu-id="ea142-130">An attempt was made to set a clip list for a DirectDrawClipper object that is already monitoring a window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-131"><span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**\_COLORKEYNOTSET DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-131"><span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR\_COLORKEYNOTSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-132">Nessuna chiave del colore di origine specificata per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="ea142-132">No source color key is specified for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-133"><span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**\_CURRENTLYNOTAVAIL DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-133"><span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR\_CURRENTLYNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-134">Attualmente non è disponibile alcun supporto.</span><span class="sxs-lookup"><span data-stu-id="ea142-134">No support is currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-135"><span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**\_DDSCAPSCOMPLEXREQUIRED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-135"><span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR\_DDSCAPSCOMPLEXREQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-136">Novità per DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="ea142-136">New for DirectX 7.0.</span></span> <span data-ttu-id="ea142-137">Per la superficie è richiesto il \_ flag complesso ddsCaps.</span><span class="sxs-lookup"><span data-stu-id="ea142-137">The surface requires the DDSCAPS\_COMPLEX flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-138"><span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**\_DCALREADYCREATED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-138"><span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR\_DCALREADYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-139">Per questa area è già stato restituito un contesto di dispositivo (DC).</span><span class="sxs-lookup"><span data-stu-id="ea142-139">A device context (DC) has already been returned for this surface.</span></span> <span data-ttu-id="ea142-140">Per ogni superficie è possibile recuperare un solo controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="ea142-140">Only one DC can be retrieved for each surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-141"><span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR \_ DEVICEDOESNTOWNSURFACE**</span><span class="sxs-lookup"><span data-stu-id="ea142-141"><span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR\_DEVICEDOESNTOWNSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-142">Le superfici create da un dispositivo DirectDraw non possono essere utilizzate direttamente da un altro dispositivo DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="ea142-142">Surfaces created by one DirectDraw device cannot be used directly by another DirectDraw device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-143"><span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR \_ DIRECTDRAWALREADYCREATED**</span><span class="sxs-lookup"><span data-stu-id="ea142-143"><span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR\_DIRECTDRAWALREADYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-144">Un oggetto DirectDraw che rappresenta questo driver è già stato creato per questo processo.</span><span class="sxs-lookup"><span data-stu-id="ea142-144">A DirectDraw object representing this driver has already been created for this process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-145"><span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**\_eccezione DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-145"><span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**DDERR\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-146">È stata rilevata un'eccezione durante l'esecuzione dell'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="ea142-146">An exception was encountered while performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-147"><span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**\_EXCLUSIVEMODEALREADYSET DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-147"><span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR\_EXCLUSIVEMODEALREADYSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-148">È stato effettuato un tentativo di impostare il livello cooperativo quando era già impostato come esclusivo.</span><span class="sxs-lookup"><span data-stu-id="ea142-148">An attempt was made to set the cooperative level when it was already set to exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-149"><span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="ea142-149"><span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-150">I dati sono scaduti e pertanto non sono più validi.</span><span class="sxs-lookup"><span data-stu-id="ea142-150">The data has expired and is therefore no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-151"><span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**\_generico DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-151"><span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-152">Si è verificata una condizione di errore non definita.</span><span class="sxs-lookup"><span data-stu-id="ea142-152">There is an undefined error condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-153"><span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**\_HEIGHTALIGN DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-153"><span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR\_HEIGHTALIGN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-154">L'altezza del rettangolo specificato non è un multiplo dell'allineamento richiesto.</span><span class="sxs-lookup"><span data-stu-id="ea142-154">The height of the provided rectangle is not a multiple of the required alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-155"><span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**\_HWNDALREADYSET DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-155"><span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR\_HWNDALREADYSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-156">L'handle di finestra a livello di cooperativa DirectDraw è già stato impostato.</span><span class="sxs-lookup"><span data-stu-id="ea142-156">The DirectDraw cooperative-level window handle has already been set.</span></span> <span data-ttu-id="ea142-157">Non può essere reimpostato mentre per il processo sono state create superfici o tavolozze.</span><span class="sxs-lookup"><span data-stu-id="ea142-157">It cannot be reset while the process has surfaces or palettes created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-158"><span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**\_HWNDSUBCLASSED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-158"><span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR\_HWNDSUBCLASSED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-159">È stato impedito il ripristino dello stato di DirectDraw perché l'handle di finestra a livello di cooperativo DirectDraw è stato sottoclassato.</span><span class="sxs-lookup"><span data-stu-id="ea142-159">DirectDraw is prevented from restoring state because the DirectDraw cooperative-level window handle has been subclassed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-160"><span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**\_IMPLICITLYCREATED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-160"><span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR\_IMPLICITLYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-161">Impossibile ripristinare la superficie perché è una superficie creata in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="ea142-161">The surface cannot be restored because it is an implicitly created surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-162"><span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**\_INCOMPATIBLEPRIMARY DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-162"><span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR\_INCOMPATIBLEPRIMARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-163">La richiesta di creazione della superficie primaria non corrisponde alla superficie primaria esistente.</span><span class="sxs-lookup"><span data-stu-id="ea142-163">The primary surface creation request does not match the existing primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-164"><span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**\_INVALIDCAPS DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-164"><span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**DDERR\_INVALIDCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-165">Uno o più bit della funzionalità passati alla funzione di callback non sono corretti.</span><span class="sxs-lookup"><span data-stu-id="ea142-165">One or more of the capability bits passed to the callback function are incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-166"><span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**\_INVALIDCLIPLIST DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-166"><span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR\_INVALIDCLIPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-167">DirectDraw non supporta l'elenco di clip fornito.</span><span class="sxs-lookup"><span data-stu-id="ea142-167">DirectDraw does not support the provided clip list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-168"><span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**\_INVALIDDIRECTDRAWGUID DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-168"><span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR\_INVALIDDIRECTDRAWGUID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-169">L'identificatore univoco globale (GUID) passato alla funzione [**DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) non è un identificatore di driver DirectDraw valido.</span><span class="sxs-lookup"><span data-stu-id="ea142-169">The globally unique identifier (GUID) passed to the [**DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) function is not a valid DirectDraw driver identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-170"><span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**\_INVALIDMODE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-170"><span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR\_INVALIDMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-171">DirectDraw non supporta la modalità richiesta.</span><span class="sxs-lookup"><span data-stu-id="ea142-171">DirectDraw does not support the requested mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-172"><span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**\_INVALIDOBJECT DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-172"><span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR\_INVALIDOBJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-173">DirectDraw ha ricevuto un puntatore che era un oggetto DirectDraw non valido.</span><span class="sxs-lookup"><span data-stu-id="ea142-173">DirectDraw received a pointer that was an invalid DirectDraw object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-174"><span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**\_INVALIDPARAMS DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-174"><span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR\_INVALIDPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-175">Uno o più parametri passati al metodo non sono corretti.</span><span class="sxs-lookup"><span data-stu-id="ea142-175">One or more of the parameters passed to the method are incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-176"><span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**\_INVALIDPIXELFORMAT DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-176"><span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR\_INVALIDPIXELFORMAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-177">Il formato pixel non è valido come specificato.</span><span class="sxs-lookup"><span data-stu-id="ea142-177">The pixel format was invalid as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-178"><span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**\_INVALIDPOSITION DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-178"><span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR\_INVALIDPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-179">La posizione della sovrimpressione nella destinazione non è più valida.</span><span class="sxs-lookup"><span data-stu-id="ea142-179">The position of the overlay on the destination is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-180"><span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**\_INVALIDRECT DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-180"><span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR\_INVALIDRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-181">Il rettangolo specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="ea142-181">The provided rectangle was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-182"><span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**\_INVALIDSTREAM DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-182"><span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR\_INVALIDSTREAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-183">Il flusso specificato contiene dati non validi.</span><span class="sxs-lookup"><span data-stu-id="ea142-183">The specified stream contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-184"><span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**\_INVALIDSURFACETYPE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-184"><span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR\_INVALIDSURFACETYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-185">Il tipo della superficie è errato.</span><span class="sxs-lookup"><span data-stu-id="ea142-185">The surface was of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-186"><span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**\_LOCKEDSURFACES DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-186"><span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR\_LOCKEDSURFACES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-187">Una o più superfici sono bloccate, causando l'errore dell'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="ea142-187">One or more surfaces are locked, causing the failure of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-188"><span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**\_MOREDATA DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-188"><span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR\_MOREDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-189">Sono disponibili più dati delle dimensioni del buffer specificate.</span><span class="sxs-lookup"><span data-stu-id="ea142-189">There is more data available than the specified buffer size can hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-190"><span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**\_NewMode DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-190"><span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR\_NEWMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-191">Novità per DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="ea142-191">New for DirectX 7.0.</span></span> <span data-ttu-id="ea142-192">Quando [**IDirectDraw7:: StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) viene chiamato con il \_ flag DDSMT ISTESTREQUIRED, potrebbe restituire questo valore per indicare che alcune o tutte le risoluzioni possono e devono essere testate.</span><span class="sxs-lookup"><span data-stu-id="ea142-192">When [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) is called with the DDSMT\_ISTESTREQUIRED flag, it might return this value to denote that some or all of the resolutions can and should be tested.</span></span> <span data-ttu-id="ea142-193">[**IDirectDraw7:: EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) restituisce questo valore per indicare che il test è stato impostato su una nuova modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea142-193">[**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) returns this value to indicate that the test has switched to a new display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-194"><span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**\_NO3D DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-194"><span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR\_NO3D**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-195">Non è presente alcun hardware o emulazione 3D.</span><span class="sxs-lookup"><span data-stu-id="ea142-195">No 3-D hardware or emulation is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-196"><span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**\_NOALPHAHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-196"><span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR\_NOALPHAHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-197">Non è presente alcun hardware di accelerazione Alpha, che causa l'errore dell'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="ea142-197">No alpha-acceleration hardware is present or available, causing the failure of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-198"><span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**\_NOBLTHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-198"><span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR\_NOBLTHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-199">Nessun blocco di bit che trasferisce hardware è presente.</span><span class="sxs-lookup"><span data-stu-id="ea142-199">No bit block transferring hardware is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-200"><span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR \_ NOclips**</span><span class="sxs-lookup"><span data-stu-id="ea142-200"><span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR\_NOCLIPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-201">Non è disponibile alcun elenco di clip.</span><span class="sxs-lookup"><span data-stu-id="ea142-201">No clip list is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-202"><span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**\_NOCLIPPERATTACHED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-202"><span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR\_NOCLIPPERATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-203">Nessun oggetto DirectDrawClipper associato all'oggetto Surface.</span><span class="sxs-lookup"><span data-stu-id="ea142-203">No DirectDrawClipper object is attached to the surface object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-204"><span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**\_NOCOLORCONVHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-204"><span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR\_NOCOLORCONVHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-205">Non sono presenti componenti hardware per la conversione di colori.</span><span class="sxs-lookup"><span data-stu-id="ea142-205">No color-conversion hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-206"><span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**\_NOCOLORKEY DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-206"><span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR\_NOCOLORKEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-207">La superficie non dispone attualmente di una chiave di colore.</span><span class="sxs-lookup"><span data-stu-id="ea142-207">The surface does not currently have a color key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-208"><span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**\_NOCOLORKEYHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-208"><span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR\_NOCOLORKEYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-209">Non è disponibile alcun supporto hardware per la chiave di colore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ea142-209">There is no hardware support for the destination color key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-210"><span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**\_NOCOOPERATIVELEVELSET DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-210"><span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR\_NOCOOPERATIVELEVELSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-211">È stata chiamata una funzione create senza il metodo [**IDirectDraw7:: SetCooperativeLevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) .</span><span class="sxs-lookup"><span data-stu-id="ea142-211">A create function was called without the [**IDirectDraw7::SetCooperativeLevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-212"><span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**\_NODC DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-212"><span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR\_NODC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-213">Non è mai stato creato alcun contesto di dispositivo (DC) per questa superficie.</span><span class="sxs-lookup"><span data-stu-id="ea142-213">No device context (DC) has ever been created for this surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-214"><span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**\_NODDROPSHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-214"><span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR\_NODDROPSHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-215">Non è disponibile alcun hardware di operazione di raster (POR) DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="ea142-215">No DirectDraw raster-operation (ROP) hardware is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-216"><span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**\_NODIRECTDRAWHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-216"><span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR\_NODIRECTDRAWHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-217">Non è possibile creare oggetti DirectDraw solo per l'hardware. il driver non supporta alcun hardware.</span><span class="sxs-lookup"><span data-stu-id="ea142-217">Hardware-only DirectDraw object creation is not possible; the driver does not support any hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-218"><span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**\_NODIRECTDRAWSUPPORT DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-218"><span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR\_NODIRECTDRAWSUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-219">Il supporto di DirectDraw non è possibile con il driver di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="ea142-219">DirectDraw support is not possible with the current display driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-220"><span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**\_NODRIVERSUPPORT DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-220"><span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR\_NODRIVERSUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-221">Novità per DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="ea142-221">New for DirectX 7.0.</span></span> <span data-ttu-id="ea142-222">Il test non può continuare perché il driver della scheda di visualizzazione non enumera le frequenze di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ea142-222">Testing cannot proceed because the display adapter driver does not enumerate refresh rates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-223"><span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**\_NOemulazione DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-223"><span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR\_NOEMULATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-224">L'emulazione software non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="ea142-224">Software emulation is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-225"><span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**\_NOEXCLUSIVEMODE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-225"><span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR\_NOEXCLUSIVEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-226">Per l'operazione è necessario che l'applicazione disponga della modalità esclusiva, ma che l'applicazione non abbia la modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="ea142-226">The operation requires the application to have exclusive mode, but the application does not have exclusive mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-227"><span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**\_NOFLIPHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-227"><span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR\_NOFLIPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-228">Il capovolgimento delle superfici visibili non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ea142-228">Flipping visible surfaces is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-229"><span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**\_NOFOCUSWINDOW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-229"><span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR\_NOFOCUSWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-230">È stato effettuato un tentativo di creare o impostare una finestra del dispositivo senza prima impostare la finestra dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="ea142-230">An attempt was made to create or set a device window without first setting the focus window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-231"><span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**\_NOGDI DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-231"><span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR\_NOGDI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-232">Non è presente alcun GDI.</span><span class="sxs-lookup"><span data-stu-id="ea142-232">No GDI is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-233"><span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR \_ NOhwnd**</span><span class="sxs-lookup"><span data-stu-id="ea142-233"><span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR\_NOHWND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-234">Per la notifica Clipper è necessario un handle di finestra o in precedenza non è stato impostato alcun handle di finestra come handle della finestra a livello cooperativo.</span><span class="sxs-lookup"><span data-stu-id="ea142-234">Clipper notification requires a window handle, or no window handle has been previously set as the cooperative level window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-235"><span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**\_NOMIPMAPHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-235"><span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR\_NOMIPMAPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-236">Nessun hardware di mapping di trama con supporto per mipmap è presente o disponibile.</span><span class="sxs-lookup"><span data-stu-id="ea142-236">No mipmap-capable texture mapping hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-237"><span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**\_NOMIRRORHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-237"><span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR\_NOMIRRORHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-238">Nessun hardware di mirroring presente o disponibile.</span><span class="sxs-lookup"><span data-stu-id="ea142-238">No mirroring hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-239"><span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**\_NOMONITORINFORMATION DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-239"><span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR\_NOMONITORINFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-240">Novità per DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="ea142-240">New for DirectX 7.0.</span></span> <span data-ttu-id="ea142-241">Il test non può continuare perché al monitoraggio non sono associati dati EDID.</span><span class="sxs-lookup"><span data-stu-id="ea142-241">Testing cannot proceed because the monitor has no associated EDID data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-242"><span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**\_NONONLOCALVIDMEM DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-242"><span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR\_NONONLOCALVIDMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-243">È stato effettuato un tentativo di allocazione della memoria video non locale da un dispositivo che non supporta la memoria video non locale.</span><span class="sxs-lookup"><span data-stu-id="ea142-243">An attempt was made to allocate nonlocal video memory from a device that does not support nonlocal video memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-244"><span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**\_NOOPTIMIZEHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-244"><span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR\_NOOPTIMIZEHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-245">Il dispositivo non supporta le superfici ottimizzate.</span><span class="sxs-lookup"><span data-stu-id="ea142-245">The device does not support optimized surfaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-246"><span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**\_NOOVERLAYDEST DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-246"><span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR\_NOOVERLAYDEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-247">Il metodo [**IDirectDrawSurface7:: GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) viene chiamato su una sovrimpressione che il metodo [**IDirectDrawSurface7:: UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) non è stato chiamato per stabilire come destinazione.</span><span class="sxs-lookup"><span data-stu-id="ea142-247">The [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) method is called on an overlay that the [**IDirectDrawSurface7::UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) method has not been called on to establish as a destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-248"><span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**\_NOOVERLAYHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-248"><span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR\_NOOVERLAYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-249">Non sono presenti hardware sovrapposti o disponibili.</span><span class="sxs-lookup"><span data-stu-id="ea142-249">No overlay hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-250"><span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**\_NOPALETTEATTACHED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-250"><span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR\_NOPALETTEATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-251">Nessun oggetto tavolozza associato a questa superficie.</span><span class="sxs-lookup"><span data-stu-id="ea142-251">No palette object is attached to this surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-252"><span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**\_NOPALETTEHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-252"><span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR\_NOPALETTEHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-253">Non è disponibile alcun supporto hardware per le tavolozze dei colori 16 o 256.</span><span class="sxs-lookup"><span data-stu-id="ea142-253">There is no hardware support for 16- or 256-color palettes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-254"><span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**\_NORASTEROPHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-254"><span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR\_NORASTEROPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-255">Non sono presenti hardware di operazioni raster appropriate o disponibili.</span><span class="sxs-lookup"><span data-stu-id="ea142-255">No appropriate raster-operation hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-256"><span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**\_NOROTATIONHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-256"><span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR\_NOROTATIONHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-257">Non è presente alcun hardware di rotazione o disponibile.</span><span class="sxs-lookup"><span data-stu-id="ea142-257">No rotation hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-258"><span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**\_NOSTEREOHARDWARE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-258"><span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR\_NOSTEREOHARDWARE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-259">Non è presente alcun hardware stereo presente o disponibile.</span><span class="sxs-lookup"><span data-stu-id="ea142-259">There is no stereo hardware present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-260"><span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**\_NOSTRETCHHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-260"><span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR\_NOSTRETCHHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-261">Non è disponibile alcun supporto hardware per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="ea142-261">There is no hardware support for stretching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-262"><span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**\_NOSURFACELEFT DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-262"><span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR\_NOSURFACELEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-263">Non sono presenti componenti hardware che supportano le superfici stereo.</span><span class="sxs-lookup"><span data-stu-id="ea142-263">There is no hardware present that supports stereo surfaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-264"><span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**\_NOT4BITCOLOR DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-264"><span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR\_NOT4BITCOLOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-265">L'oggetto DirectDrawSurface non utilizza una tavolozza dei colori a 4 bit e l'operazione richiesta richiede una tavolozza dei colori a 4 bit.</span><span class="sxs-lookup"><span data-stu-id="ea142-265">The DirectDrawSurface object is not using a 4-bit color palette, and the requested operation requires a 4-bit color palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-266"><span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**\_NOT4BITCOLORINDEX DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-266"><span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR\_NOT4BITCOLORINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-267">L'oggetto DirectDrawSurface non utilizza una tavolozza degli indici a 4 bit e l'operazione richiesta richiede una tavolozza per gli indici dei colori a 4 bit.</span><span class="sxs-lookup"><span data-stu-id="ea142-267">The DirectDrawSurface object is not using a 4-bit color index palette, and the requested operation requires a 4-bit color index palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-268"><span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**\_NOT8BITCOLOR DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-268"><span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR\_NOT8BITCOLOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-269">L'oggetto DirectDrawSurface non utilizza una tavolozza dei colori a 8 bit e l'operazione richiesta richiede una tavolozza dei colori a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="ea142-269">The DirectDrawSurface object is not using an 8-bit color palette, and the requested operation requires an 8-bit color palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-270"><span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**\_NOTAOVERLAYSURFACE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-270"><span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR\_NOTAOVERLAYSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-271">Per una superficie non sovrapposta viene chiamato un componente overlay.</span><span class="sxs-lookup"><span data-stu-id="ea142-271">An overlay component is called for a nonoverlay surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-272"><span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**\_NOTEXTUREHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-272"><span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR\_NOTEXTUREHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-273">Non è possibile eseguire l'operazione perché non è presente alcun hardware di mapping delle trame o disponibile.</span><span class="sxs-lookup"><span data-stu-id="ea142-273">The operation cannot be carried out because no texture-mapping hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-274"><span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**\_NOTFLIPPABLE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-274"><span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR\_NOTFLIPPABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-275">È stato effettuato un tentativo di capovolgere una superficie che non può essere capovolta.</span><span class="sxs-lookup"><span data-stu-id="ea142-275">An attempt was made to flip a surface that cannot be flipped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-276"><span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**\_NotFound DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-276"><span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-277">Elemento richiesto non trovato.</span><span class="sxs-lookup"><span data-stu-id="ea142-277">The requested item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-278"><span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**\_NOTINITIALIZED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-278"><span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR\_NOTINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-279">È stato effettuato un tentativo di chiamare un metodo di interfaccia di un oggetto DirectDraw creato da [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) prima dell'inizializzazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ea142-279">An attempt was made to call an interface method of a DirectDraw object created by [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) before the object was initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-280"><span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**\_NOTLOADED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-280"><span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR\_NOTLOADED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-281">La superficie è una superficie ottimizzata, ma non è ancora stata allocata memoria.</span><span class="sxs-lookup"><span data-stu-id="ea142-281">The surface is an optimized surface, but it has not yet been allocated any memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-282"><span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**\_NOTLOCKED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-282"><span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR\_NOTLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-283">È stato effettuato un tentativo di sbloccare una superficie non bloccata.</span><span class="sxs-lookup"><span data-stu-id="ea142-283">An attempt was made to unlock a surface that was not locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-284"><span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**\_NOTPAGELOCKED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-284"><span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR\_NOTPAGELOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-285">È stato effettuato un tentativo di sblocco di una superficie senza blocchi di pagina in attesa.</span><span class="sxs-lookup"><span data-stu-id="ea142-285">An attempt was made to page-unlock a surface with no outstanding page locks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-286"><span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**\_NOTPALETTIZED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-286"><span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR\_NOTPALETTIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-287">La superficie utilizzata non è una superficie basata su tavolozza.</span><span class="sxs-lookup"><span data-stu-id="ea142-287">The surface being used is not a palette-based surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-288"><span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**\_NOVSYNCHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-288"><span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR\_NOVSYNCHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-289">Non è disponibile alcun supporto hardware per le operazioni di sincronizzazione vuote verticali.</span><span class="sxs-lookup"><span data-stu-id="ea142-289">There is no hardware support for vertical blank synchronized operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-290"><span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**\_NOZBUFFERHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-290"><span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR\_NOZBUFFERHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-291">Non è possibile eseguire l'operazione di creazione di un buffer z nella memoria di visualizzazione o di un trasferimento a blocchi di bit (BitBlt), usando un buffer z perché non è disponibile alcun supporto hardware per i buffer z.</span><span class="sxs-lookup"><span data-stu-id="ea142-291">The operation to create a z-buffer in display memory or to perform a bit block transfer (bitblt), using a z-buffer cannot be carried out because there is no hardware support for z-buffers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-292"><span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**\_NOZOVERLAYHW DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-292"><span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR\_NOZOVERLAYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-293">Le superfici sovrapposte non possono essere a livello z, in base all'ordine z perché l'hardware non supporta l'ordinamento z delle sovrapposizioni.</span><span class="sxs-lookup"><span data-stu-id="ea142-293">The overlay surfaces cannot be z-layered, based on the z-order because the hardware does not support z-ordering of overlays.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-294"><span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**\_OUTOFCAPS DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-294"><span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**DDERR\_OUTOFCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-295">L'hardware necessario per l'operazione richiesta è già stato allocato.</span><span class="sxs-lookup"><span data-stu-id="ea142-295">The hardware needed for the requested operation has already been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-296"><span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**\_OutOfMemory DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-296"><span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**DDERR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-297">DirectDraw non dispone di memoria sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ea142-297">DirectDraw does not have enough memory to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-298"><span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**\_OUTOFVIDEOMEMORY DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-298"><span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR\_OUTOFVIDEOMEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-299">DirectDraw non dispone di memoria di visualizzazione sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ea142-299">DirectDraw does not have enough display memory to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-300"><span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**\_OVERLAPPINGRECTS DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-300"><span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR\_OVERLAPPINGRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-301">I rettangoli di origine e di destinazione si trovano nella stessa superficie e si sovrappongono.</span><span class="sxs-lookup"><span data-stu-id="ea142-301">The source and destination rectangles are on the same surface and overlap each other.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-302"><span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**\_OVERLAYCANTCLIP DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-302"><span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**DDERR\_OVERLAYCANTCLIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-303">L'hardware non supporta le sovrapposizioni ritagliate.</span><span class="sxs-lookup"><span data-stu-id="ea142-303">The hardware does not support clipped overlays.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-304"><span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**\_OVERLAYCOLORKEYONLYONEACTIVE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-304"><span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR\_OVERLAYCOLORKEYONLYONEACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-305">È stato effettuato un tentativo di avere più di una chiave di colore attiva in una sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="ea142-305">An attempt was made to have more than one color key active on an overlay.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-306"><span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**\_OVERLAYNOTVISIBLE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-306"><span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**DDERR\_OVERLAYNOTVISIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-307">Il metodo [**IDirectDrawSurface7:: GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) è stato chiamato su una sovrapposizione nascosta.</span><span class="sxs-lookup"><span data-stu-id="ea142-307">The [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) method was called on a hidden overlay.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-308"><span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**\_PALETTEBUSY DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-308"><span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**DDERR\_PALETTEBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-309">L'accesso a questa tavolozza è stato rifiutato perché la tavolozza è bloccata da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="ea142-309">Access to this palette is refused because the palette is locked by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-310"><span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**\_PRIMARYSURFACEALREADYEXISTS DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-310"><span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR\_PRIMARYSURFACEALREADYEXISTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-311">Questo processo ha già creato una superficie primaria.</span><span class="sxs-lookup"><span data-stu-id="ea142-311">This process has already created a primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-312"><span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**\_REGIONTOOSMALL DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-312"><span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**DDERR\_REGIONTOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-313">L'area passata al metodo [**IDirectDrawClipper:: getclipart**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) è troppo piccola.</span><span class="sxs-lookup"><span data-stu-id="ea142-313">The region passed to the [**IDirectDrawClipper::GetClipList**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) method is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-314"><span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**\_SURFACEALREADYATTACHED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-314"><span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR\_SURFACEALREADYATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-315">È stato effettuato un tentativo di collegare una superficie a un'altra superficie a cui è già collegata.</span><span class="sxs-lookup"><span data-stu-id="ea142-315">An attempt was made to attach a surface to another surface to which it is already attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-316"><span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**\_SURFACEALREADYDEPENDENT DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-316"><span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR\_SURFACEALREADYDEPENDENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-317">È stato effettuato un tentativo di rendere una superficie una dipendenza da un'altra superficie su cui è già dipendente.</span><span class="sxs-lookup"><span data-stu-id="ea142-317">An attempt was made to make a surface a dependency of another surface on which it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-318"><span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**\_SURFACEBUSY DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-318"><span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR\_SURFACEBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-319">L'accesso alla superficie viene rifiutato perché la superficie è bloccata da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="ea142-319">Access to the surface is refused because the surface is locked by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-320"><span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**\_SURFACEISOBSCURED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-320"><span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR\_SURFACEISOBSCURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-321">L'accesso alla superficie viene rifiutato perché la superficie è nascosta.</span><span class="sxs-lookup"><span data-stu-id="ea142-321">Access to the surface is refused because the surface is obscured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-322"><span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**\_SURFACELOST DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-322"><span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR\_SURFACELOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-323">L'accesso alla superficie viene rifiutato perché la memoria della superficie è sparita.</span><span class="sxs-lookup"><span data-stu-id="ea142-323">Access to the surface is refused because the surface memory is gone.</span></span> <span data-ttu-id="ea142-324">Chiamare il metodo [**IDirectDrawSurface7:: Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) su questa superficie per ripristinare la memoria associata.</span><span class="sxs-lookup"><span data-stu-id="ea142-324">Call the [**IDirectDrawSurface7::Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) method on this surface to restore the memory associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-325"><span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**\_SURFACENOTATTACHED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-325"><span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR\_SURFACENOTATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-326">La superficie richiesta non è collegata.</span><span class="sxs-lookup"><span data-stu-id="ea142-326">The requested surface is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-327"><span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**\_TESTFINISHED DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-327"><span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR\_TESTFINISHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-328">Novità per DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="ea142-328">New for DirectX 7.0.</span></span> <span data-ttu-id="ea142-329">Quando viene restituito dal metodo [**IDirectDraw7:: StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) , questo valore indica che non è stato possibile avviare alcun test perché tutte le risoluzioni selezionate per il test hanno già le informazioni sulla frequenza di aggiornamento nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ea142-329">When returned by the [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) method, this value means that no test could be initiated because all the resolutions chosen for testing already have refresh rate information in the registry.</span></span> <span data-ttu-id="ea142-330">Quando viene restituito da [**IDirectDraw7:: EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode), il valore indica che DirectDraw ha completato un test della frequenza di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ea142-330">When returned by [**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode), the value means that DirectDraw has completed a refresh rate test.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-331"><span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**\_TOOBIGHEIGHT DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-331"><span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR\_TOOBIGHEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-332">L'altezza richiesta da DirectDraw è troppo grande.</span><span class="sxs-lookup"><span data-stu-id="ea142-332">The height requested by DirectDraw is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-333"><span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**\_TOOBIGSIZE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-333"><span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR\_TOOBIGSIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-334">La dimensione richiesta da DirectDraw è troppo grande.</span><span class="sxs-lookup"><span data-stu-id="ea142-334">The size requested by DirectDraw is too large.</span></span> <span data-ttu-id="ea142-335">Tuttavia, l'altezza e la larghezza individuali sono dimensioni valide.</span><span class="sxs-lookup"><span data-stu-id="ea142-335">However, the individual height and width are valid sizes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-336"><span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**\_TOOBIGWIDTH DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-336"><span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR\_TOOBIGWIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-337">La larghezza richiesta da DirectDraw è troppo grande.</span><span class="sxs-lookup"><span data-stu-id="ea142-337">The width requested by DirectDraw is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-338"><span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="ea142-338"><span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-339">L'operazione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="ea142-339">The operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-340"><span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**\_UNSUPPORTEDFORMAT DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-340"><span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR\_UNSUPPORTEDFORMAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-341">Il formato pixel richiesto non è supportato da DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="ea142-341">The pixel format requested is not supported by DirectDraw.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-342"><span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**\_UNSUPPORTEDMASK DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-342"><span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR\_UNSUPPORTEDMASK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-343">La maschera di maschera nel formato pixel richiesta non è supportata da DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="ea142-343">The bitmask in the pixel format requested is not supported by DirectDraw.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-344"><span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**\_UNSUPPORTEDMODE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-344"><span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR\_UNSUPPORTEDMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-345">La visualizzazione è attualmente in modalità non supportata.</span><span class="sxs-lookup"><span data-stu-id="ea142-345">The display is currently in an unsupported mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-346"><span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**\_VERTICALBLANKINPROGRESS DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-346"><span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR\_VERTICALBLANKINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-347">È in corso uno spazio vuoto verticale.</span><span class="sxs-lookup"><span data-stu-id="ea142-347">A vertical blank is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-348"><span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**\_VIDEONOTACTIVE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-348"><span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**DDERR\_VIDEONOTACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-349">La porta video non è attiva.</span><span class="sxs-lookup"><span data-stu-id="ea142-349">The video port is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-350"><span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**\_WASSTILLDRAWING DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-350"><span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR\_WASSTILLDRAWING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-351">L'operazione BitBlt precedente che sta trasferendo informazioni da o verso questa superficie non è completa.</span><span class="sxs-lookup"><span data-stu-id="ea142-351">The previous bitblt operation that is transferring information to or from this surface is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-352"><span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**\_WRONGMODE DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-352"><span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR\_WRONGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-353">Impossibile ripristinare la superficie perché è stata creata in una modalità diversa.</span><span class="sxs-lookup"><span data-stu-id="ea142-353">This surface cannot be restored because it was created in a different mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea142-354"><span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**\_XALIGN DDERR**</span><span class="sxs-lookup"><span data-stu-id="ea142-354"><span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR\_XALIGN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ea142-355">Il rettangolo specificato non è stato allineato orizzontalmente su un limite obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ea142-355">The provided rectangle was not horizontally aligned on a required boundary.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea142-356">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea142-356">Requirements</span></span>



| <span data-ttu-id="ea142-357">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea142-357">Requirement</span></span> | <span data-ttu-id="ea142-358">Valore</span><span class="sxs-lookup"><span data-stu-id="ea142-358">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea142-359">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea142-359">Header</span></span><br/> | <dl> <span data-ttu-id="ea142-360"><dt>Ddraw. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea142-360"><dt>Ddraw.h</dt></span></span> </dl> |



 

