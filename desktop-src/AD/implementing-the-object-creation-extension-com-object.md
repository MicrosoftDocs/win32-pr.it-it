---
title: Implementazione dell'oggetto COM di estensione per la creazione di oggetti
description: Un'estensione per la creazione di oggetti è un oggetto COM implementato come server in-process. Le estensioni per la creazione di oggetti primari e secondari devono implementare l'interfaccia IDsAdminNewObjExt.
ms.assetid: 0a8ed0ed-9dcb-4373-b549-7da3f3d9f641
ms.tgt_platform: multiple
keywords:
- Implementazione dell'oggetto COM dell'estensione per la creazione di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c1a9da94caa300c1277cf6f6030357ca9d573d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046503"
---
# <a name="implementing-the-object-creation-extension-com-object"></a>Implementazione dell'oggetto COM di estensione per la creazione di oggetti

Un'estensione per la creazione di oggetti è un oggetto COM implementato come server in-process. Le estensioni per la creazione di oggetti primari e secondari devono implementare l'interfaccia [**IDsAdminNewObjExt**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) .

## <a name="implementing-idsadminnewobjext"></a>Implementazione di IDsAdminNewObjExt

Quando viene creata la creazione guidata oggetto, viene inizializzata ogni estensione per la creazione di oggetti chiamando il metodo [**IDsAdminNewObjExt:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize) dell'estensione. Il metodo **Initialize** fornisce l'estensione con informazioni sul contenitore in cui viene creato l'oggetto, il nome della classe del nuovo oggetto e le informazioni sulla procedura guidata stessa. Se la creazione guidata oggetto viene avviata per creare un nuovo oggetto da un oggetto esistente, il parametro *pADsCopySource* non sarà **null**. In questo caso, l'estensione deve tentare di ottenere tutti i dati dall'oggetto copiato come possibile.

Dopo l'inizializzazione dell'estensione, viene chiamato il metodo [**IDsAdminNewObjExt:: AddPages**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-addpages) . Durante questo metodo, l'estensione deve aggiungere la pagina o le pagine alla procedura guidata. Una pagina della procedura guidata viene creata compilando una struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) e passando la struttura alla funzione [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . La pagina viene quindi aggiunta alla procedura guidata chiamando la funzione di callback che viene passata a **AddPages** nel parametro *lpfnAddPage* .

Prima che venga visualizzata la pagina di estensione, viene chiamato [**IDsAdminNewObjExt:: seobject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) . Questa operazione fornisce l'estensione con un puntatore di interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) per l'oggetto da creare.

Quando viene visualizzata la pagina della procedura guidata, la pagina deve gestire e rispondere a tutti i messaggi di notifica necessari della procedura guidata, ad esempio [**PSN \_ seactive**](../controls/psn-setactive.md) e [**PSN \_ WIZNEXT**](../controls/psn-wiznext.md).

Al termine di tutte le pagine della procedura guidata, la procedura guidata visualizzerà una pagina di completamento che fornisce un riepilogo dei dati immessi. Questa procedura guidata consente di ottenere questi dati chiamando il metodo [**IDsAdminNewObjExt:: GetSummaryInfo**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-getsummaryinfo) per ognuna delle estensioni. Il metodo **GetSummaryInfo** fornisce un **BSTR** che contiene i dati di testo visualizzati nella pagina "Finish". Non è necessario che un'estensione per la creazione di oggetti fornisca dati di riepilogo. In questo caso, **GetSummaryInfo** deve restituire **E \_ NOTIMPL**. **GetSummaryInfo** viene chiamato solo una volta per ogni estensione, non per pagina, pertanto se l'estensione per la creazione di oggetti aggiunge più di una pagina, l'estensione deve combinare i dati di riepilogo in una sola stringa.

Quando l'utente fa clic sul pulsante **fine** nella pagina "Finish" (fine), la procedura guidata chiama ognuno dei metodi [**IDsAdminNewObjExt:: WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) dell'estensione con il contesto di **\_ \_ \_ precommit DSA NEWOBJ CTX** . In questo caso, l'estensione deve scrivere i dati raccolti nelle proprietà appropriate usando il metodo [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) o [**IADs::P UTEX**](/windows/desktop/api/iads/nf-iads-iads-putex) . L'interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) viene fornita all'estensione nel metodo [**IDsAdminNewObjExt::**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) SetValue. L'estensione non deve eseguire il commit delle proprietà memorizzate nella cache chiamando [**IADs:: seinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo). Quando tutte le proprietà sono state scritte, l'estensione per la creazione di oggetti primari esegue il commit delle modifiche chiamando **IADs:: SetInfo**. Questo argomento viene trattato in modo più dettagliato di seguito.

Se si verifica un errore, l'estensione riceverà una notifica dell'errore e durante il quale l'operazione si è verificata quando viene chiamato il metodo [**IDsAdminNewObjExt:: OnError**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-onerror) .

## <a name="implementing-a-primary-object-creation-wizard"></a>Implementazione di una procedura guidata di creazione di oggetti primari

L'implementazione di una procedura guidata di creazione di un oggetto primario è identica a una procedura guidata di creazione di un oggetto secondario, con la differenza che una procedura guidata di creazione di oggetti primari deve eseguire alcuni passaggi.

Prima che la prima pagina venisse rilasciata, la creazione guidata oggetto deve creare l'oggetto directory temporanea. A tale scopo, chiamare il metodo [**IDsAdminNewObjPrimarySite:: CreateNew**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-createnew) . Un puntatore all'interfaccia [**IDsAdminNewObjPrimarySite**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjprimarysite) viene ottenuto chiamando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) con **IID \_ IDsAdminNewObjPrimarySite** sull'interfaccia [**IDsAdminNewObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobj) passata a [**IDsAdminNewObjExt:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize). Il metodo **CreateNew** crea un nuovo oggetto temporaneo e chiama [**IDsAdminNewObjExt:: seobject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) per ogni estensione.

Quando una procedura guidata di creazione di un oggetto contiene più di una pagina, il sistema implementa una pagina di completamento che visualizza un riepilogo delle informazioni sull'oggetto da salvare. Quando si fa clic sul pulsante **fine** nella pagina "Finish" (fine), il sistema chiamerà ogni metodo [**IDsAdminNewObjExt:: WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) dell'estensione per la creazione di oggetti e quindi eseguirà il commit dell'oggetto temporaneo nella memoria persistente. Se, tuttavia, la creazione guidata oggetto contiene solo una pagina, nella pagina verranno visualizzati i pulsanti **OK** e **Annulla** anziché i pulsanti **indietro**, **Avanti** e **Annulla** normalmente presenti in una procedura guidata e non viene fornita alcuna pagina "fine". Per questo motivo, una procedura guidata per l'estensione per la creazione di oggetti a pagina singola deve chiamare [**IDsAdminNewObjPrimarySite:: commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) per eseguire le operazioni di scrittura e salvataggio. Un'estensione per la creazione di oggetti primari a pagina singola deve chiamare il **commit** in risposta alla notifica [**\_ WIZFINISH PSN**](../controls/psn-wizfinish.md) .

Poiché altre estensioni per la creazione di oggetti possono aggiungere pagine alla procedura guidata, l'estensione per la creazione di oggetti primari potrebbe non essere in grado di stabilire se sono presenti più pagine nella procedura guidata. Questo non è un problema per due motivi: prima di tutto, se il sistema implementa la pagina "fine", l'estensione per la creazione di oggetti primari riceverà la notifica [**\_ WIZNEXT PSN**](../controls/psn-wiznext.md) invece della notifica **\_ WIZNEXT PSN** . In secondo luogo, il [**commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) non verrà eseguito in modalità innocua se la procedura guidata contiene più di una pagina.

 

 