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
# <a name="directdraw-return-codes"></a>Codici restituiti di DirectDraw

Gli errori sono rappresentati da valori negativi e non possono essere combinati. In questa tabella sono elencati i valori che possono essere restituiti da tutti i metodi delle [interfacce DirectDraw](directdraw-interfaces.md) e delle [funzioni DirectDraw](directdraw-functions.md). Per un elenco dei codici di errore che possono essere restituiti da ogni metodo o funzione, vedere la descrizione del metodo o della funzione.

<dl> <dt>

<span id="DD_OK"></span><span id="dd_ok"></span>**DD \_ OK**
</dt> <dd> <dl> <dt>



La richiesta è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**\_ALREADYINITIALIZED DDERR**
</dt> <dd> <dl> <dt>



L'oggetto è già stato inizializzato.


</dt> </dl> </dd> <dt>

<span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**\_BLTFASTCANTCLIP DDERR**
</dt> <dd> <dl> <dt>



Un oggetto DirectDrawClipper è associato a una superficie di origine che è passata a una chiamata al metodo [**IDirectDrawSurface7:: BltFast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) .


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**\_CANNOTATTACHSURFACE DDERR**
</dt> <dd> <dl> <dt>



Non è possibile collegare una superficie a un'altra superficie richiesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**\_CANNOTDETACHSURFACE DDERR**
</dt> <dd> <dl> <dt>



Non è possibile scollegare una superficie da un'altra superficie richiesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**\_CANTCREATEDC DDERR**
</dt> <dd> <dl> <dt>



Windows non è in grado di creare altri contesti di dispositivo o un controller di dominio ha richiesto una superficie indicizzata della tavolozza quando la superficie non aveva una tavolozza e la modalità di visualizzazione non è stata indicizzata (in questo caso, DirectDraw non è in grado di selezionare una tavolozza appropriata nel controller di dominio).


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**\_CANTDUPLICATE DDERR**
</dt> <dd> <dl> <dt>



Non è possibile duplicare le superfici primarie e 3D, o le superfici create in modo implicito.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**\_CANTLOCKSURFACE DDERR**
</dt> <dd> <dl> <dt>



L'accesso a questa superficie è stato rifiutato perché è stato effettuato un tentativo di bloccare la superficie primaria senza il supporto per l'interfaccia di controllo di visualizzazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**\_CANTPAGELOCK DDERR**
</dt> <dd> <dl> <dt>



Tentativo di blocco di una superficie di pagina non riuscito. Il blocco di pagina non funziona in una superficie di memoria di visualizzazione o in una superficie primaria emulata.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**\_CANTPAGEUNLOCK DDERR**
</dt> <dd> <dl> <dt>



Tentativo di sblocco di una superficie non riuscito. Lo sblocco della pagina non funziona in una superficie di memoria di visualizzazione o in una superficie primaria emulata.


</dt> </dl> </dd> <dt>

<span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**\_CLIPPERISUSINGHWND DDERR**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di impostare un elenco di clip per un oggetto DirectDrawClipper che sta già monitorando un handle di finestra.


</dt> </dl> </dd> <dt>

<span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**\_COLORKEYNOTSET DDERR**
</dt> <dd> <dl> <dt>



Nessuna chiave del colore di origine specificata per questa operazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**\_CURRENTLYNOTAVAIL DDERR**
</dt> <dd> <dl> <dt>



Attualmente non è disponibile alcun supporto.


</dt> </dl> </dd> <dt>

<span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**\_DDSCAPSCOMPLEXREQUIRED DDERR**
</dt> <dd> <dl> <dt>



Novità per DirectX 7,0. Per la superficie è richiesto il \_ flag complesso ddsCaps.


</dt> </dl> </dd> <dt>

<span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**\_DCALREADYCREATED DDERR**
</dt> <dd> <dl> <dt>



Per questa area è già stato restituito un contesto di dispositivo (DC). Per ogni superficie è possibile recuperare un solo controller di dominio.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR \_ DEVICEDOESNTOWNSURFACE**
</dt> <dd> <dl> <dt>



Le superfici create da un dispositivo DirectDraw non possono essere utilizzate direttamente da un altro dispositivo DirectDraw.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR \_ DIRECTDRAWALREADYCREATED**
</dt> <dd> <dl> <dt>



Un oggetto DirectDraw che rappresenta questo driver è già stato creato per questo processo.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**\_eccezione DDERR**
</dt> <dd> <dl> <dt>



È stata rilevata un'eccezione durante l'esecuzione dell'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**\_EXCLUSIVEMODEALREADYSET DDERR**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di impostare il livello cooperativo quando era già impostato come esclusivo.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR \_ scaduto**
</dt> <dd> <dl> <dt>



I dati sono scaduti e pertanto non sono più validi.


</dt> </dl> </dd> <dt>

<span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**\_generico DDERR**
</dt> <dd> <dl> <dt>



Si è verificata una condizione di errore non definita.


</dt> </dl> </dd> <dt>

<span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**\_HEIGHTALIGN DDERR**
</dt> <dd> <dl> <dt>



L'altezza del rettangolo specificato non è un multiplo dell'allineamento richiesto.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**\_HWNDALREADYSET DDERR**
</dt> <dd> <dl> <dt>



L'handle di finestra a livello di cooperativa DirectDraw è già stato impostato. Non può essere reimpostato mentre per il processo sono state create superfici o tavolozze.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**\_HWNDSUBCLASSED DDERR**
</dt> <dd> <dl> <dt>



È stato impedito il ripristino dello stato di DirectDraw perché l'handle di finestra a livello di cooperativo DirectDraw è stato sottoclassato.


</dt> </dl> </dd> <dt>

<span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**\_IMPLICITLYCREATED DDERR**
</dt> <dd> <dl> <dt>



Impossibile ripristinare la superficie perché è una superficie creata in modo implicito.


</dt> </dl> </dd> <dt>

<span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**\_INCOMPATIBLEPRIMARY DDERR**
</dt> <dd> <dl> <dt>



La richiesta di creazione della superficie primaria non corrisponde alla superficie primaria esistente.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**\_INVALIDCAPS DDERR**
</dt> <dd> <dl> <dt>



Uno o più bit della funzionalità passati alla funzione di callback non sono corretti.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**\_INVALIDCLIPLIST DDERR**
</dt> <dd> <dl> <dt>



DirectDraw non supporta l'elenco di clip fornito.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**\_INVALIDDIRECTDRAWGUID DDERR**
</dt> <dd> <dl> <dt>



L'identificatore univoco globale (GUID) passato alla funzione [**DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) non è un identificatore di driver DirectDraw valido.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**\_INVALIDMODE DDERR**
</dt> <dd> <dl> <dt>



DirectDraw non supporta la modalità richiesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**\_INVALIDOBJECT DDERR**
</dt> <dd> <dl> <dt>



DirectDraw ha ricevuto un puntatore che era un oggetto DirectDraw non valido.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**\_INVALIDPARAMS DDERR**
</dt> <dd> <dl> <dt>



Uno o più parametri passati al metodo non sono corretti.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**\_INVALIDPIXELFORMAT DDERR**
</dt> <dd> <dl> <dt>



Il formato pixel non è valido come specificato.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**\_INVALIDPOSITION DDERR**
</dt> <dd> <dl> <dt>



La posizione della sovrimpressione nella destinazione non è più valida.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**\_INVALIDRECT DDERR**
</dt> <dd> <dl> <dt>



Il rettangolo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**\_INVALIDSTREAM DDERR**
</dt> <dd> <dl> <dt>



Il flusso specificato contiene dati non validi.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**\_INVALIDSURFACETYPE DDERR**
</dt> <dd> <dl> <dt>



Il tipo della superficie è errato.


</dt> </dl> </dd> <dt>

<span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**\_LOCKEDSURFACES DDERR**
</dt> <dd> <dl> <dt>



Una o più superfici sono bloccate, causando l'errore dell'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**\_MOREDATA DDERR**
</dt> <dd> <dl> <dt>



Sono disponibili più dati delle dimensioni del buffer specificate.


</dt> </dl> </dd> <dt>

<span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**\_NewMode DDERR**
</dt> <dd> <dl> <dt>



Novità per DirectX 7,0. Quando [**IDirectDraw7:: StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) viene chiamato con il \_ flag DDSMT ISTESTREQUIRED, potrebbe restituire questo valore per indicare che alcune o tutte le risoluzioni possono e devono essere testate. [**IDirectDraw7:: EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) restituisce questo valore per indicare che il test è stato impostato su una nuova modalità di visualizzazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**\_NO3D DDERR**
</dt> <dd> <dl> <dt>



Non è presente alcun hardware o emulazione 3D.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**\_NOALPHAHW DDERR**
</dt> <dd> <dl> <dt>



Non è presente alcun hardware di accelerazione Alpha, che causa l'errore dell'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**\_NOBLTHW DDERR**
</dt> <dd> <dl> <dt>



Nessun blocco di bit che trasferisce hardware è presente.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR \_ NOclips**
</dt> <dd> <dl> <dt>



Non è disponibile alcun elenco di clip.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**\_NOCLIPPERATTACHED DDERR**
</dt> <dd> <dl> <dt>



Nessun oggetto DirectDrawClipper associato all'oggetto Surface.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**\_NOCOLORCONVHW DDERR**
</dt> <dd> <dl> <dt>



Non sono presenti componenti hardware per la conversione di colori.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**\_NOCOLORKEY DDERR**
</dt> <dd> <dl> <dt>



La superficie non dispone attualmente di una chiave di colore.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**\_NOCOLORKEYHW DDERR**
</dt> <dd> <dl> <dt>



Non è disponibile alcun supporto hardware per la chiave di colore di destinazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**\_NOCOOPERATIVELEVELSET DDERR**
</dt> <dd> <dl> <dt>



È stata chiamata una funzione create senza il metodo [**IDirectDraw7:: SetCooperativeLevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) .


</dt> </dl> </dd> <dt>

<span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**\_NODC DDERR**
</dt> <dd> <dl> <dt>



Non è mai stato creato alcun contesto di dispositivo (DC) per questa superficie.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**\_NODDROPSHW DDERR**
</dt> <dd> <dl> <dt>



Non è disponibile alcun hardware di operazione di raster (POR) DirectDraw.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**\_NODIRECTDRAWHW DDERR**
</dt> <dd> <dl> <dt>



Non è possibile creare oggetti DirectDraw solo per l'hardware. il driver non supporta alcun hardware.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**\_NODIRECTDRAWSUPPORT DDERR**
</dt> <dd> <dl> <dt>



Il supporto di DirectDraw non è possibile con il driver di visualizzazione corrente.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**\_NODRIVERSUPPORT DDERR**
</dt> <dd> <dl> <dt>



Novità per DirectX 7,0. Il test non può continuare perché il driver della scheda di visualizzazione non enumera le frequenze di aggiornamento.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**\_NOemulazione DDERR**
</dt> <dd> <dl> <dt>



L'emulazione software non è disponibile.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**\_NOEXCLUSIVEMODE DDERR**
</dt> <dd> <dl> <dt>



Per l'operazione è necessario che l'applicazione disponga della modalità esclusiva, ma che l'applicazione non abbia la modalità esclusiva.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**\_NOFLIPHW DDERR**
</dt> <dd> <dl> <dt>



Il capovolgimento delle superfici visibili non è supportato.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**\_NOFOCUSWINDOW DDERR**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di creare o impostare una finestra del dispositivo senza prima impostare la finestra dello stato attivo.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**\_NOGDI DDERR**
</dt> <dd> <dl> <dt>



Non è presente alcun GDI.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR \_ NOhwnd**
</dt> <dd> <dl> <dt>



Per la notifica Clipper è necessario un handle di finestra o in precedenza non è stato impostato alcun handle di finestra come handle della finestra a livello cooperativo.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**\_NOMIPMAPHW DDERR**
</dt> <dd> <dl> <dt>



Nessun hardware di mapping di trama con supporto per mipmap è presente o disponibile.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**\_NOMIRRORHW DDERR**
</dt> <dd> <dl> <dt>



Nessun hardware di mirroring presente o disponibile.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**\_NOMONITORINFORMATION DDERR**
</dt> <dd> <dl> <dt>



Novità per DirectX 7,0. Il test non può continuare perché al monitoraggio non sono associati dati EDID.


</dt> </dl> </dd> <dt>

<span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**\_NONONLOCALVIDMEM DDERR**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di allocazione della memoria video non locale da un dispositivo che non supporta la memoria video non locale.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**\_NOOPTIMIZEHW DDERR**
</dt> <dd> <dl> <dt>



Il dispositivo non supporta le superfici ottimizzate.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**\_NOOVERLAYDEST DDERR**
</dt> <dd> <dl> <dt>



Il metodo [**IDirectDrawSurface7:: GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) viene chiamato su una sovrimpressione che il metodo [**IDirectDrawSurface7:: UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) non è stato chiamato per stabilire come destinazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**\_NOOVERLAYHW DDERR**
</dt> <dd> <dl> <dt>



Non sono presenti hardware sovrapposti o disponibili.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**\_NOPALETTEATTACHED DDERR**
</dt> <dd> <dl> <dt>



Nessun oggetto tavolozza associato a questa superficie.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**\_NOPALETTEHW DDERR**
</dt> <dd> <dl> <dt>



Non è disponibile alcun supporto hardware per le tavolozze dei colori 16 o 256.


</dt> </dl> </dd> <dt>

<span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**\_NORASTEROPHW DDERR**
</dt> <dd> <dl> <dt>



Non sono presenti hardware di operazioni raster appropriate o disponibili.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**\_NOROTATIONHW DDERR**
</dt> <dd> <dl> <dt>



Non è presente alcun hardware di rotazione o disponibile.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**\_NOSTEREOHARDWARE DDERR**
</dt> <dd> <dl> <dt>



Non è presente alcun hardware stereo presente o disponibile.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**\_NOSTRETCHHW DDERR**
</dt> <dd> <dl> <dt>



Non è disponibile alcun supporto hardware per l'estensione.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**\_NOSURFACELEFT DDERR**
</dt> <dd> <dl> <dt>



Non sono presenti componenti hardware che supportano le superfici stereo.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**\_NOT4BITCOLOR DDERR**
</dt> <dd> <dl> <dt>



L'oggetto DirectDrawSurface non utilizza una tavolozza dei colori a 4 bit e l'operazione richiesta richiede una tavolozza dei colori a 4 bit.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**\_NOT4BITCOLORINDEX DDERR**
</dt> <dd> <dl> <dt>



L'oggetto DirectDrawSurface non utilizza una tavolozza degli indici a 4 bit e l'operazione richiesta richiede una tavolozza per gli indici dei colori a 4 bit.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**\_NOT8BITCOLOR DDERR**
</dt> <dd> <dl> <dt>



L'oggetto DirectDrawSurface non utilizza una tavolozza dei colori a 8 bit e l'operazione richiesta richiede una tavolozza dei colori a 8 bit.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**\_NOTAOVERLAYSURFACE DDERR**
</dt> <dd> <dl> <dt>



Per una superficie non sovrapposta viene chiamato un componente overlay.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**\_NOTEXTUREHW DDERR**
</dt> <dd> <dl> <dt>



Non è possibile eseguire l'operazione perché non è presente alcun hardware di mapping delle trame o disponibile.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**\_NOTFLIPPABLE DDERR**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di capovolgere una superficie che non può essere capovolta.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**\_NotFound DDERR**
</dt> <dd> <dl> <dt>



Elemento richiesto non trovato.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**\_NOTINITIALIZED DDERR**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di chiamare un metodo di interfaccia di un oggetto DirectDraw creato da [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) prima dell'inizializzazione dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**\_NOTLOADED DDERR**
</dt> <dd> <dl> <dt>



La superficie è una superficie ottimizzata, ma non è ancora stata allocata memoria.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**\_NOTLOCKED DDERR**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di sbloccare una superficie non bloccata.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**\_NOTPAGELOCKED DDERR**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di sblocco di una superficie senza blocchi di pagina in attesa.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**\_NOTPALETTIZED DDERR**
</dt> <dd> <dl> <dt>



La superficie utilizzata non è una superficie basata su tavolozza.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**\_NOVSYNCHW DDERR**
</dt> <dd> <dl> <dt>



Non è disponibile alcun supporto hardware per le operazioni di sincronizzazione vuote verticali.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**\_NOZBUFFERHW DDERR**
</dt> <dd> <dl> <dt>



Non è possibile eseguire l'operazione di creazione di un buffer z nella memoria di visualizzazione o di un trasferimento a blocchi di bit (BitBlt), usando un buffer z perché non è disponibile alcun supporto hardware per i buffer z.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**\_NOZOVERLAYHW DDERR**
</dt> <dd> <dl> <dt>



Le superfici sovrapposte non possono essere a livello z, in base all'ordine z perché l'hardware non supporta l'ordinamento z delle sovrapposizioni.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**\_OUTOFCAPS DDERR**
</dt> <dd> <dl> <dt>



L'hardware necessario per l'operazione richiesta è già stato allocato.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**\_OutOfMemory DDERR**
</dt> <dd> <dl> <dt>



DirectDraw non dispone di memoria sufficiente per eseguire l'operazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**\_OUTOFVIDEOMEMORY DDERR**
</dt> <dd> <dl> <dt>



DirectDraw non dispone di memoria di visualizzazione sufficiente per eseguire l'operazione.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**\_OVERLAPPINGRECTS DDERR**
</dt> <dd> <dl> <dt>



I rettangoli di origine e di destinazione si trovano nella stessa superficie e si sovrappongono.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**\_OVERLAYCANTCLIP DDERR**
</dt> <dd> <dl> <dt>



L'hardware non supporta le sovrapposizioni ritagliate.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**\_OVERLAYCOLORKEYONLYONEACTIVE DDERR**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di avere più di una chiave di colore attiva in una sovrimpressione.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**\_OVERLAYNOTVISIBLE DDERR**
</dt> <dd> <dl> <dt>



Il metodo [**IDirectDrawSurface7:: GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) è stato chiamato su una sovrapposizione nascosta.


</dt> </dl> </dd> <dt>

<span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**\_PALETTEBUSY DDERR**
</dt> <dd> <dl> <dt>



L'accesso a questa tavolozza è stato rifiutato perché la tavolozza è bloccata da un altro thread.


</dt> </dl> </dd> <dt>

<span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**\_PRIMARYSURFACEALREADYEXISTS DDERR**
</dt> <dd> <dl> <dt>



Questo processo ha già creato una superficie primaria.


</dt> </dl> </dd> <dt>

<span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**\_REGIONTOOSMALL DDERR**
</dt> <dd> <dl> <dt>



L'area passata al metodo [**IDirectDrawClipper:: getclipart**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) è troppo piccola.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**\_SURFACEALREADYATTACHED DDERR**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di collegare una superficie a un'altra superficie a cui è già collegata.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**\_SURFACEALREADYDEPENDENT DDERR**
</dt> <dd> <dl> <dt>



È stato effettuato un tentativo di rendere una superficie una dipendenza da un'altra superficie su cui è già dipendente.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**\_SURFACEBUSY DDERR**
</dt> <dd> <dl> <dt>



L'accesso alla superficie viene rifiutato perché la superficie è bloccata da un altro thread.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**\_SURFACEISOBSCURED DDERR**
</dt> <dd> <dl> <dt>



L'accesso alla superficie viene rifiutato perché la superficie è nascosta.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**\_SURFACELOST DDERR**
</dt> <dd> <dl> <dt>



L'accesso alla superficie viene rifiutato perché la memoria della superficie è sparita. Chiamare il metodo [**IDirectDrawSurface7:: Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) su questa superficie per ripristinare la memoria associata.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**\_SURFACENOTATTACHED DDERR**
</dt> <dd> <dl> <dt>



La superficie richiesta non è collegata.


</dt> </dl> </dd> <dt>

<span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**\_TESTFINISHED DDERR**
</dt> <dd> <dl> <dt>



Novità per DirectX 7,0. Quando viene restituito dal metodo [**IDirectDraw7:: StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) , questo valore indica che non è stato possibile avviare alcun test perché tutte le risoluzioni selezionate per il test hanno già le informazioni sulla frequenza di aggiornamento nel registro di sistema. Quando viene restituito da [**IDirectDraw7:: EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode), il valore indica che DirectDraw ha completato un test della frequenza di aggiornamento.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**\_TOOBIGHEIGHT DDERR**
</dt> <dd> <dl> <dt>



L'altezza richiesta da DirectDraw è troppo grande.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**\_TOOBIGSIZE DDERR**
</dt> <dd> <dl> <dt>



La dimensione richiesta da DirectDraw è troppo grande. Tuttavia, l'altezza e la larghezza individuali sono dimensioni valide.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**\_TOOBIGWIDTH DDERR**
</dt> <dd> <dl> <dt>



La larghezza richiesta da DirectDraw è troppo grande.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR non \_ supportato**
</dt> <dd> <dl> <dt>



L'operazione non è supportata.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**\_UNSUPPORTEDFORMAT DDERR**
</dt> <dd> <dl> <dt>



Il formato pixel richiesto non è supportato da DirectDraw.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**\_UNSUPPORTEDMASK DDERR**
</dt> <dd> <dl> <dt>



La maschera di maschera nel formato pixel richiesta non è supportata da DirectDraw.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**\_UNSUPPORTEDMODE DDERR**
</dt> <dd> <dl> <dt>



La visualizzazione è attualmente in modalità non supportata.


</dt> </dl> </dd> <dt>

<span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**\_VERTICALBLANKINPROGRESS DDERR**
</dt> <dd> <dl> <dt>



È in corso uno spazio vuoto verticale.


</dt> </dl> </dd> <dt>

<span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**\_VIDEONOTACTIVE DDERR**
</dt> <dd> <dl> <dt>



La porta video non è attiva.


</dt> </dl> </dd> <dt>

<span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**\_WASSTILLDRAWING DDERR**
</dt> <dd> <dl> <dt>



L'operazione BitBlt precedente che sta trasferendo informazioni da o verso questa superficie non è completa.


</dt> </dl> </dd> <dt>

<span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**\_WRONGMODE DDERR**
</dt> <dd> <dl> <dt>



Impossibile ripristinare la superficie perché è stata creata in una modalità diversa.


</dt> </dl> </dd> <dt>

<span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**\_XALIGN DDERR**
</dt> <dd> <dl> <dt>



Il rettangolo specificato non è stato allineato orizzontalmente su un limite obbligatorio.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Ddraw. h</dt> </dl> |



 

