---
title: Codici restituiti DirectDraw (Ddraw.h)
description: 'Codici restituiti DirectDraw: gli errori sono rappresentati da valori negativi e non possono essere combinati.'
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
ms.openlocfilehash: 1e937ad9cc32a7837303d535b73b176c7e16f2d0ab0033bf625f629d2d5f7bc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504353"
---
# <a name="directdraw-return-codes"></a>Codici restituiti directdraw

Gli errori sono rappresentati da valori negativi e non possono essere combinati. In questa tabella sono elencati i valori che possono essere restituiti da tutti i metodi delle interfacce [DirectDraw e](directdraw-interfaces.md) [delle funzioni DirectDraw](directdraw-functions.md). Per un elenco dei codici di errore che ogni metodo o funzione può restituire, vedere la descrizione del metodo o della funzione.

<dl> <dt>

<span id="DD_OK"></span><span id="dd_ok"></span>**DD \_ OK**
</dt> <dd> <dl> <dt>



La richiesta è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR \_ GIÀ INIZIALIZZATO**
</dt> <dd> <dl> <dt>



L'oggetto è già stato inizializzato.


</dt> </dl> </dd> <dt>

<span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR \_ BLTFASTCANTCLIP**
</dt> <dd> <dl> <dt>



Un oggetto DirectDrawClipper è associato a una superficie di origine passata in una chiamata al metodo [**IDirectDrawSurface7::BltFast.**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast)


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR \_ CANNOTATTACHSURFACE**
</dt> <dd> <dl> <dt>



Una superficie non può essere collegata a un'altra superficie richiesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR \_ CANNOTDETACHSURFACE**
</dt> <dd> <dl> <dt>



Una superficie non può essere scollegata da un'altra superficie richiesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR \_ CANTCREATEDC**
</dt> <dd> <dl> <dt>



Windows non è possibile creare altri contesti di dispositivo o un controller di dominio ha richiesto una superficie indicizzata con tavolozza quando la superficie non dispone di una tavolozza e la modalità di visualizzazione non è stata indicizzata con il riquadro ( in questo caso DirectDraw non può selezionare una tavolozza appropriata nel controller di dominio).


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR \_ CANTDUPLICATE**
</dt> <dd> <dl> <dt>



Le superfici primarie e 3D, o superfici create in modo implicito, non possono essere duplicate.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR \_ CANTLOCKSURFACE**
</dt> <dd> <dl> <dt>



L'accesso a questa superficie viene rifiutato perché è stato effettuato un tentativo di bloccare la superficie primaria senza supporto DCI (Display Control Interface).


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR \_ CANTPAGELOCK**
</dt> <dd> <dl> <dt>



Tentativo di blocco della pagina di una superficie non riuscito. Il blocco di pagina non funziona su una superficie di memoria di visualizzazione o su una superficie primaria emulata.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR \_ CANTPAGEUNLOCK**
</dt> <dd> <dl> <dt>



Tentativo di sblocco della pagina di una superficie non riuscito. Lo sblocco della pagina non funziona su una superficie di memoria di visualizzazione o su una superficie primaria emulata.


</dt> </dl> </dd> <dt>

<span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR \_ CLIPPERISUSINGHWND**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di impostare un elenco di clip per un oggetto DirectDrawClipper che sta già monitorando un handle di finestra.


</dt> </dl> </dd> <dt>

<span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR \_ COLORKEYNOTSET**
</dt> <dd> <dl> <dt>



Nessuna chiave di colore di origine specificata per questa operazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR \_ ATTUALMENTE NON DISPONIBILE**
</dt> <dd> <dl> <dt>



Non è attualmente disponibile alcun supporto.


</dt> </dl> </dd> <dt>

<span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR \_ DDSCAPSCOMPLEXREQUIRED**
</dt> <dd> <dl> <dt>



Novità di DirectX 7.0. La superficie richiede il flag COMPLEX DDSCAPS. \_


</dt> </dl> </dd> <dt>

<span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR \_ DCALREADYCREATED**
</dt> <dd> <dl> <dt>



Un contesto di dispositivo (DC) è già stato restituito per questa superficie. È possibile recuperare un solo controller di dominio per ogni superficie.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR \_ DEVICEDOESN TOWNSURFACE**
</dt> <dd> <dl> <dt>



Le superfici create da un dispositivo DirectDraw non possono essere usate direttamente da un altro dispositivo DirectDraw.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR \_ DIRECTDRAWALREADYCREATED**
</dt> <dd> <dl> <dt>



Per questo processo è già stato creato un oggetto DirectDraw che rappresenta questo driver.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**ECCEZIONE \_ DDERR**
</dt> <dd> <dl> <dt>



Si è verificata un'eccezione durante l'esecuzione dell'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR \_ EXCLUSIVEMODEALREADYSET**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di impostare il livello cooperativo quando era già impostato su esclusivo.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR \_ SCADUTO**
</dt> <dd> <dl> <dt>



I dati sono scaduti e pertanto non sono più validi.


</dt> </dl> </dd> <dt>

<span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR \_ GENERIC**
</dt> <dd> <dl> <dt>



È presente una condizione di errore non definita.


</dt> </dl> </dd> <dt>

<span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR \_ HEIGHTALIGN**
</dt> <dd> <dl> <dt>



L'altezza del rettangolo specificato non è un multiplo dell'allineamento richiesto.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR \_ HWNDALREADYSET**
</dt> <dd> <dl> <dt>



L'handle della finestra a livello cooperativo DirectDraw è già stato impostato. Non può essere reimpostato mentre nel processo sono state create superfici o tavolozze.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR \_ HWNDSUBCLASSED**
</dt> <dd> <dl> <dt>



Non è possibile ripristinare lo stato di DirectDraw perché l'handle della finestra a livello cooperativo DirectDraw è stato sottoclassato.


</dt> </dl> </dd> <dt>

<span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR \_ CREATE IN MODO IMPLICITO**
</dt> <dd> <dl> <dt>



Non è possibile ripristinare la superficie perché è una superficie creata in modo implicito.


</dt> </dl> </dd> <dt>

<span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR \_ INCOMPATIBLEPRIMARY**
</dt> <dd> <dl> <dt>



La richiesta di creazione della superficie primaria non corrisponde alla superficie primaria esistente.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**DDERR \_ INVALIDCAPS**
</dt> <dd> <dl> <dt>



Uno o più bit di funzionalità passati alla funzione di callback non sono corretti.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR \_ INVALIDCLIPLIST**
</dt> <dd> <dl> <dt>



DirectDraw non supporta l'elenco di clip specificato.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR \_ INVALIDDIRECTDRAWGUID**
</dt> <dd> <dl> <dt>



L'identificatore univoco globale (GUID) passato alla [**funzione DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) non è un identificatore di driver DirectDraw valido.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR \_ INVALIDMODE**
</dt> <dd> <dl> <dt>



DirectDraw non supporta la modalità richiesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR \_ INVALIDOBJECT**
</dt> <dd> <dl> <dt>



DirectDraw ha ricevuto un puntatore che era un oggetto DirectDraw non valido.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR \_ INVALIDPARAMS**
</dt> <dd> <dl> <dt>



Uno o più parametri passati al metodo non sono corretti.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR \_ INVALIDPIXELFORMAT**
</dt> <dd> <dl> <dt>



Il formato pixel non è valido come specificato.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR \_ INVALIDPOSITION**
</dt> <dd> <dl> <dt>



La posizione della sovrimpressione nella destinazione non è più valida.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR \_ INVALIDRECT**
</dt> <dd> <dl> <dt>



Il rettangolo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR \_ INVALIDSTREAM**
</dt> <dd> <dl> <dt>



Il flusso specificato contiene dati non validi.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR \_ INVALIDSURFACETYPE**
</dt> <dd> <dl> <dt>



La superficie era di tipo errato.


</dt> </dl> </dd> <dt>

<span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR \_ LOCKEDSURFACES**
</dt> <dd> <dl> <dt>



Una o più superfici sono bloccate, causando l'errore dell'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR \_ MOREDATA**
</dt> <dd> <dl> <dt>



Sono disponibili più dati di quelli che possono contenere le dimensioni del buffer specificate.


</dt> </dl> </dd> <dt>

<span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR \_ NEWMODE**
</dt> <dd> <dl> <dt>



Novità di DirectX 7.0. Quando [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) viene chiamato con il \_ flag DDSMT ISTESTREQUIRED, potrebbe restituire questo valore per indicare che alcune o tutte le risoluzioni possono e devono essere testate. [**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) restituisce questo valore per indicare che il test è stato impostato su una nuova modalità di visualizzazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR \_ NO3D**
</dt> <dd> <dl> <dt>



Non sono presenti hardware o emulazione 3D.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR \_ NOALPHAHW**
</dt> <dd> <dl> <dt>



Nessun hardware di accelerazione alfa è presente o disponibile, causando l'errore dell'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR \_ NOBLTHW**
</dt> <dd> <dl> <dt>



Non è presente alcun blocco di bit che trasferisce l'hardware.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR \_ NOCLIPLIST**
</dt> <dd> <dl> <dt>



Non è disponibile alcun elenco di clip.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR \_ NOCLIPPERATTACHED**
</dt> <dd> <dl> <dt>



Nessun oggetto DirectDrawClipper è collegato all'oggetto surface.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR \_ NOCOLORCONVHW**
</dt> <dd> <dl> <dt>



Non è presente o disponibile alcun hardware per la conversione dei colori.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR \_ NOCOLORKEY**
</dt> <dd> <dl> <dt>



La superficie non dispone attualmente di una chiave di colore.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR \_ NOCOLORKEYHW**
</dt> <dd> <dl> <dt>



Non è disponibile alcun supporto hardware per la chiave di colore di destinazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR \_ NOCOOPERATIVELEVELSET**
</dt> <dd> <dl> <dt>



È stata chiamata una funzione di creazione senza [**il metodo IDirectDraw7::SetCooperativeLevel.**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel)


</dt> </dl> </dd> <dt>

<span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR \_ NODC**
</dt> <dd> <dl> <dt>



Non è mai stato creato alcun contesto di dispositivo per questa superficie.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR \_ NODDROPSHW**
</dt> <dd> <dl> <dt>



Non è disponibile alcun hardware SYSTEM (DirectDraw Raster Operation).


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR \_ NODIRECTDRAWHW**
</dt> <dd> <dl> <dt>



La creazione di oggetti DirectDraw solo hardware non è possibile. il driver non supporta hardware.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR \_ NODIRECTDRAWSUPPORT**
</dt> <dd> <dl> <dt>



Il supporto di DirectDraw non è possibile con il driver di visualizzazione corrente.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR \_ NODRIVERSUPPORT**
</dt> <dd> <dl> <dt>



Novità di DirectX 7.0. Il test non può continuare perché il driver dell'adattatore video non enumera le frequenze di aggiornamento.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR \_ NOEMULATION**
</dt> <dd> <dl> <dt>



L'emulazione del software non è disponibile.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR \_ NOEXCLUSIVEMODE**
</dt> <dd> <dl> <dt>



L'operazione richiede che l'applicazione abbia la modalità esclusiva, ma l'applicazione non ha la modalità esclusiva.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR \_ NOFLIPHW**
</dt> <dd> <dl> <dt>



Il capovolgimento delle superfici visibili non è supportato.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR \_ NOFOCUSWINDOW**
</dt> <dd> <dl> <dt>



Si è tentato di creare o impostare una finestra del dispositivo senza prima impostare la finestra attiva.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR \_ NOGDI**
</dt> <dd> <dl> <dt>



Non è presente alcun GDI.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR \_ NOHWND**
</dt> <dd> <dl> <dt>



Clipper notifica richiede un handle di finestra oppure nessun handle di finestra è stato impostato in precedenza come handle di finestra a livello cooperativo.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR \_ NOMIPMAPHW**
</dt> <dd> <dl> <dt>



Non sono presenti o disponibili hardware per il mapping di trame che supportano mipmap.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR \_ NOMIRRORHW**
</dt> <dd> <dl> <dt>



Nessun hardware di mirroring è presente o disponibile.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR \_ NOMONITORINFORMATION**
</dt> <dd> <dl> <dt>



Novità di DirectX 7.0. Il test non può continuare perché al monitoraggio non sono associati dati EDID.


</dt> </dl> </dd> <dt>

<span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR \_ NONONLOCALVIDMEM**
</dt> <dd> <dl> <dt>



Si è tentato di allocare memoria video non locale da un dispositivo che non supporta la memoria video non locale.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR \_ NOOPTIMIZEHW**
</dt> <dd> <dl> <dt>



Il dispositivo non supporta superfici ottimizzate.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR \_ NOOVERLAYDEST**
</dt> <dd> <dl> <dt>



Il [**metodo IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) viene chiamato su una sovrimpressione su cui non è stato chiamato il metodo [**IDirectDrawSurface7::UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) per stabilire come destinazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR \_ NOOVERLAYHW**
</dt> <dd> <dl> <dt>



Non è presente o disponibile alcun hardware di sovrapposizione.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR \_ NOPALETTEATTACHED**
</dt> <dd> <dl> <dt>



Nessun oggetto tavolozza è collegato a questa superficie.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR \_ NOPALETTEHW**
</dt> <dd> <dl> <dt>



Non è disponibile alcun supporto hardware per le tavolozze a 16 o 256 colori.


</dt> </dl> </dd> <dt>

<span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR \_ NORASTEROPHW**
</dt> <dd> <dl> <dt>



Non è presente o disponibile alcun hardware raster-operation appropriato.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR \_ NOROTATIONHW**
</dt> <dd> <dl> <dt>



Nessun hardware di rotazione è presente o disponibile.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR \_ NOSTEREOHARDWARE**
</dt> <dd> <dl> <dt>



Non è presente o disponibile alcun hardware stereo.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR \_ NOSTRETCHHW**
</dt> <dd> <dl> <dt>



Non è disponibile alcun supporto hardware per l'estensione.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR \_ NOSURFACELEFT**
</dt> <dd> <dl> <dt>



Non è presente alcun hardware che supporti le superfici stereo.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR \_ NOT4BITCOLOR**
</dt> <dd> <dl> <dt>



L'oggetto DirectDrawSurface non usa una tavolozza dei colori a 4 bit e l'operazione richiesta richiede una tavolozza dei colori a 4 bit.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR \_ NOT4BITCOLORINDEX**
</dt> <dd> <dl> <dt>



L'oggetto DirectDrawSurface non usa una tavolozza dell'indice colori a 4 bit e l'operazione richiesta richiede una tavolozza dell'indice colori a 4 bit.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR \_ NOT8BITCOLOR**
</dt> <dd> <dl> <dt>



L'oggetto DirectDrawSurface non usa una tavolozza dei colori a 8 bit e l'operazione richiesta richiede una tavolozza dei colori a 8 bit.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR \_ NOTAOVERLAYSURFACE**
</dt> <dd> <dl> <dt>



Un componente di sovrimpressione viene chiamato per una superficie non sovrapposta.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR \_ NOTEXTUREHW**
</dt> <dd> <dl> <dt>



L'operazione non può essere eseguita perché non è presente o disponibile alcun hardware per il mapping della trama.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR \_ NOTFLIPPABLE**
</dt> <dd> <dl> <dt>



Si è tentato di capovolgere una superficie che non può essere capovolta.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR \_ NOTFOUND**
</dt> <dd> <dl> <dt>



Elemento richiesto non trovato.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR \_ NON INIZIALIZZATO**
</dt> <dd> <dl> <dt>



Si è tentato di chiamare un metodo di interfaccia di un oggetto DirectDraw creato da [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) prima dell'inizializzazione dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR \_ NON CARICATO**
</dt> <dd> <dl> <dt>



La superficie è una superficie ottimizzata, ma non è ancora stata allocata memoria.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR \_ NOTLOCKED**
</dt> <dd> <dl> <dt>



Si è tentato di sbloccare una superficie non bloccata.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR \_ NOTPAGELOCKED**
</dt> <dd> <dl> <dt>



Si è tentato di sbloccare una superficie senza blocchi di pagina in sospeso.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR \_ NOTPALETTIZED**
</dt> <dd> <dl> <dt>



La superficie usata non è una superficie basata sulla tavolozza.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR \_ NOVSYNCHW**
</dt> <dd> <dl> <dt>



Non è disponibile alcun supporto hardware per le operazioni sincronizzate verticali vuote.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR \_ NOZBUFFERHW**
</dt> <dd> <dl> <dt>



L'operazione per creare un z-buffer nella memoria di visualizzazione o per eseguire un trasferimento di blocchi di bit (bitblt), l'uso di un z-buffer non può essere eseguita perché non è disponibile alcun supporto hardware per z-buffer.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR \_ NOZOVERLAYHW**
</dt> <dd> <dl> <dt>



Le superfici di sovrimpressione non possono essere a livelli z, in base all'ordine z perché l'hardware non supporta l'ordinamento z delle sovrimpressione.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**DDERR \_ OUTOFCAPS**
</dt> <dd> <dl> <dt>



L'hardware necessario per l'operazione richiesta è già stato allocato.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**DDERR \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>



DirectDraw non dispone di memoria sufficiente per eseguire l'operazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR \_ OUTOFVIDEOMEMORY**
</dt> <dd> <dl> <dt>



DirectDraw non dispone di memoria di visualizzazione sufficiente per eseguire l'operazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR \_ OVERLAPPINGRECTS**
</dt> <dd> <dl> <dt>



I rettangoli di origine e di destinazione sono sulla stessa superficie e si sovrappongono.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**\_SOVRIMPRESSIONE DDERRANTECLIP**
</dt> <dd> <dl> <dt>



L'hardware non supporta le sovrapposizioni ritagliate.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**\_SOVRIMPRESSIONE DDERRCOLORKEYONLYONEACTIVE**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di avere più di una chiave di colore attiva in una sovrimpressione.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**\_SOVRIMPRESSIONE DDERRNOTVISIBLE**
</dt> <dd> <dl> <dt>



Il [**metodo IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) è stato chiamato su una sovrimpressione nascosta.


</dt> </dl> </dd> <dt>

<span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**DDERR \_ PALETTEBUSY**
</dt> <dd> <dl> <dt>



L'accesso a questo riquadro viene rifiutato perché il riquadro è bloccato da un altro thread.


</dt> </dl> </dd> <dt>

<span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR \_ PRIMARYSURFACEALREADYEXISTS**
</dt> <dd> <dl> <dt>



Questo processo ha già creato una superficie primaria.


</dt> </dl> </dd> <dt>

<span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**AREA \_ DDERRTOOSMALL**
</dt> <dd> <dl> <dt>



L'area passata al [**metodo IDirectDrawClipper::GetClipList**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) è troppo piccola.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR \_ SURFACEALREADYATTACHED**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di collegare una superficie a un'altra superficie a cui è già collegata.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR \_ SURFACEALREADYDEPENDENT**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di rendere una superficie una dipendenza di un'altra superficie da cui è già dipendente.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR \_ SURFACEBUSY**
</dt> <dd> <dl> <dt>



L'accesso alla superficie viene rifiutato perché la superficie è bloccata da un altro thread.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**SUPERFICIE \_ DDERRISOBSCURED**
</dt> <dd> <dl> <dt>



L'accesso alla superficie viene rifiutato perché la superficie è nascosta.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR \_ SURFACELOST**
</dt> <dd> <dl> <dt>



L'accesso alla superficie viene rifiutato perché la memoria della superficie non è più disponibile. Chiamare il [**metodo IDirectDrawSurface7::Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) su questa superficie per ripristinare la memoria associata.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR \_ SURFACENOTATTACHED**
</dt> <dd> <dl> <dt>



La superficie richiesta non è collegata.


</dt> </dl> </dd> <dt>

<span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**TEST \_ DDERRFINISHED**
</dt> <dd> <dl> <dt>



Novità di DirectX 7.0. Quando viene restituito dal metodo [**IDirectDraw7::StartModeTest,**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) questo valore indica che non è stato possibile avviare alcun test perché tutte le risoluzioni scelte per i test hanno già informazioni sulla frequenza di aggiornamento nel Registro di sistema. Quando viene restituito [**da IDirectDraw7::EvaluateMode,**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode)il valore indica che DirectDraw ha completato un test della frequenza di aggiornamento.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR \_ TOOBIGHEIGHT**
</dt> <dd> <dl> <dt>



L'altezza richiesta da DirectDraw è troppo grande.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR \_ TOOBIGSIZE**
</dt> <dd> <dl> <dt>



Le dimensioni richieste da DirectDraw sono troppo grandi. Tuttavia, le singole dimensioni di altezza e larghezza sono valide.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR \_ TOOBIGWIDTH**
</dt> <dd> <dl> <dt>



La larghezza richiesta da DirectDraw è troppo grande.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR \_ NON SUPPORTATO**
</dt> <dd> <dl> <dt>



L'operazione non è supportata.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR \_ UNSUPPORTEDFORMAT**
</dt> <dd> <dl> <dt>



Il formato pixel richiesto non è supportato da DirectDraw.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR \_ UNSUPPORTEDMASK**
</dt> <dd> <dl> <dt>



La maschera di bit nel formato pixel richiesto non è supportata da DirectDraw.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR \_ UNSUPPORTEDMODE**
</dt> <dd> <dl> <dt>



La visualizzazione è attualmente in modalità non supportata.


</dt> </dl> </dd> <dt>

<span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR \_ VERTICALBLANKINPROGRESS**
</dt> <dd> <dl> <dt>



È in corso uno spazio vuoto verticale.


</dt> </dl> </dd> <dt>

<span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**VIDEO \_ DDERRNOTACTIVE**
</dt> <dd> <dl> <dt>



La porta video non è attiva.


</dt> </dl> </dd> <dt>

<span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR \_ WASSTILLDRAWING**
</dt> <dd> <dl> <dt>



L'operazione bitblt precedente che trasferisce informazioni da o verso questa superficie è incompleta.


</dt> </dl> </dd> <dt>

<span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR \_ WRONGMODE**
</dt> <dd> <dl> <dt>



Questa superficie non può essere ripristinata perché è stata creata in una modalità diversa.


</dt> </dl> </dd> <dt>

<span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR \_ XALIGN**
</dt> <dd> <dl> <dt>



Il rettangolo specificato non era allineato orizzontalmente su un limite obbligatorio.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Ddraw.h</dt> </dl> |



 

