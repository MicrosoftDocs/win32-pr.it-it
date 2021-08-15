---
title: Implementazione dell'oggetto COM dell'estensione per la creazione di oggetti
description: Un'estensione per la creazione di oggetti è un oggetto COM implementato come server in-process. Sia le estensioni per la creazione di oggetti primari che secondari devono implementare l'interfaccia IDsAdminNewObjExt.
ms.assetid: 0a8ed0ed-9dcb-4373-b549-7da3f3d9f641
ms.tgt_platform: multiple
keywords:
- Implementazione dell'oggetto COM Object AD dell'estensione per la creazione di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c1d7eb9d3e2fe80e721068f39746e08f0ecf5a1db721658c02ec52aca39687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187639"
---
# <a name="implementing-the-object-creation-extension-com-object"></a>Implementazione dell'oggetto COM dell'estensione per la creazione di oggetti

Un'estensione per la creazione di oggetti è un oggetto COM implementato come server in-process. Sia le estensioni per la creazione di oggetti primari che secondari devono implementare [**l'interfaccia IDsAdminNewObjExt.**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext)

## <a name="implementing-idsadminnewobjext"></a>Implementazione di IDsAdminNewObjExt

Quando viene creata, la creazione guidata dell'oggetto inizializza ogni estensione per la creazione di oggetti chiamando il metodo [**IDsAdminNewObjExt::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize) dell'estensione. Il **metodo Initialize** fornisce all'estensione informazioni sul contenitore in cui viene creato l'oggetto, sul nome della classe del nuovo oggetto e sulle informazioni sulla procedura guidata stessa. Se viene avviata la creazione guidata oggetto per creare un nuovo oggetto da un oggetto esistente, il *parametro pADsCopySource* non sarà **NULL.** In questo caso, l'estensione deve tentare di ottenere la quantità di dati dall'oggetto copiato come possibile.

Dopo l'inizializzazione dell'estensione, viene chiamato il metodo [**IDsAdminNewObjExt::AddPages.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-addpages) L'estensione deve aggiungere la pagina o le pagine alla procedura guidata durante questo metodo. Viene creata una pagina della procedura guidata compilando una [**struttura PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) e quindi passando questa struttura alla [**funzione CreatePropertySheetPage.**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) La pagina viene quindi aggiunta alla procedura guidata chiamando la funzione di callback passata a **AddPages** nel *parametro lpfnAddPage.*

Prima che venga visualizzata la pagina di estensione, [**viene chiamato IDsAdminNewObjExt::SetObject.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) In questo modo l'estensione viene fornita con un puntatore a interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) per l'oggetto creato.

Mentre viene visualizzata la pagina della procedura guidata, la pagina deve gestire e rispondere a eventuali messaggi di notifica della procedura guidata necessari, ad esempio [**PSN \_ SETACTIVE**](../controls/psn-setactive.md) e [**PSN \_ WIZNEXT.**](../controls/psn-wiznext.md)

Quando l'utente completa tutte le pagine della procedura guidata, nella procedura guidata verrà visualizzata una pagina "Fine" che fornisce un riepilogo dei dati immessi. La procedura guidata ottiene questi dati chiamando il [**metodo IDsAdminNewObjExt::GetSummaryInfo**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-getsummaryinfo) per ognuna delle estensioni. Il **metodo GetSummaryInfo** fornisce un **BSTR che** contiene i dati di testo visualizzati nella pagina "Fine". Un'estensione per la creazione di oggetti non deve fornire dati di riepilogo. In questo caso, **GetSummaryInfo** deve restituire **E \_ NOTIMPL**. **GetSummaryInfo** viene chiamato una sola volta per ogni estensione, non per pagina, quindi se l'estensione per la creazione di oggetti aggiunge più di una pagina, l'estensione deve combinare i dati di riepilogo in un'unica stringa.

Quando l'utente  fa clic sul pulsante Fine nella pagina "Fine", la procedura guidata chiama ognuno dei metodi [**IDsAdminNewObjExt::WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) dell'estensione con il contesto **DSA \_ NEWOBJ \_ CTX \_ PRECOMMIT.** In questo caso, l'estensione deve scrivere i dati raccolti nelle proprietà appropriate usando il metodo [**IADs::P ut**](/windows/desktop/api/iads/nf-iads-iads-put) o [**IADs::P utEx.**](/windows/desktop/api/iads/nf-iads-iads-putex) [**L'interfaccia IADs**](/windows/desktop/api/iads/nn-iads-iads) viene fornita all'estensione nel [**metodo IDsAdminNewObjExt::SetObject.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) L'estensione non deve eseguire il commit delle proprietà memorizzate nella cache [**chiamando IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo). Dopo aver scritto tutte le proprietà, l'estensione per la creazione di oggetti primaria esegue il commit delle modifiche **chiamando IADs::SetInfo**. Questa operazione è descritta più dettagliatamente di seguito.

Se si verifica un errore, l'estensione riceverà una notifica dell'errore e durante l'operazione eseguita quando viene chiamato il metodo [**IDsAdminNewObjExt::OnError.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-onerror)

## <a name="implementing-a-primary-object-creation-wizard"></a>Implementazione di una Creazione guidata oggetto primario

L'implementazione di una creazione guidata di oggetti primari è identica a una procedura guidata per la creazione di oggetti secondari, ad eccezione del fatto che una procedura guidata per la creazione di oggetti primari deve eseguire alcuni passaggi aggiuntivi.

Prima che la prima pagina venga chiusa, la creazione guidata dell'oggetto deve creare l'oggetto directory temporaneo. A tale scopo, chiamare il [**metodo IDsAdminNewObjPrimarySite::CreateNew.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-createnew) Un puntatore all'interfaccia [**IDsAdminNewObjPrimarySite**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjprimarysite) viene ottenuto chiamando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) con **IID \_ IDsAdminNewObjPrimarySite** sull'interfaccia [**IDsAdminNewObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobj) passata a [**IDsAdminNewObjExt::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize). Il **metodo CreateNew** crea un nuovo oggetto temporaneo e chiama [**IDsAdminNewObjExt::SetObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) per ogni estensione.

Quando una creazione guidata oggetto contiene più di una pagina, il sistema implementa una pagina "Fine" che visualizza un riepilogo delle informazioni sull'oggetto da salvare. Quando  si fa clic sul pulsante Fine nella pagina "Fine", il sistema chiamerà il metodo [**IDsAdminNewObjExt::WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) dell'estensione per la creazione di oggetti e quindi eseguirà il commit dell'oggetto temporaneo nella memoria persistente. Se, tuttavia, la creazione guidata di oggetti contiene una  sola pagina, nella  pagina  saranno disponibili i pulsanti **OK** e Annulla anziché i pulsanti Indietro **,** Avanti e Annulla normalmente presenti in una procedura guidata e non viene fornita alcuna pagina "Fine". Per questo scopo, una procedura guidata di estensione per la creazione di oggetti a pagina singola deve chiamare [**IDsAdminNewObjPrimarySite::Commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) per eseguire le operazioni di scrittura e salvataggio. Un'estensione per la creazione di oggetti primari a pagina singola deve chiamare **Commit** in risposta alla notifica [**\_ PSN WIZFINISH.**](../controls/psn-wizfinish.md)

Poiché altre estensioni per la creazione di oggetti possono aggiungere pagine alla procedura guidata, l'estensione per la creazione di oggetti primaria potrebbe non sapere se è presente più di una pagina nella procedura guidata. Questo non è un problema per due motivi: innanzitutto, se il sistema implementa la pagina "Fine", l'estensione per la creazione di oggetti primaria riceverà la notifica [**PSN \_ WIZNEXT**](../controls/psn-wiznext.md) anziché la notifica **\_ PSN WIZNEXT.** In secondo momento, [**il commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) avrà esito negativo innocuo se la procedura guidata contiene più di una pagina.

 

 