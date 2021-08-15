---
title: Interfaccia IWMProfile
description: L'interfaccia IWMProfile è l'interfaccia principale per un oggetto profilo.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- Interfaccia IWMProfile windows Media Format
- Interfaccia IWMProfile windows Media Format , descritto
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: 525cdee41be011e373c65e508e91087082c17f2ec279195e2a9ab285b391fd54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084718"
---
# <a name="iwmprofile-interface"></a>Interfaccia IWMProfile

**L'interfaccia IWMProfile** è l'interfaccia principale per un [*oggetto*](wmformat-glossary.md) profilo. Un oggetto profilo viene usato per configurare profili personalizzati. È possibile usare **IWMProfile per** creare, eliminare o modificare oggetti di configurazione del flusso e oggetti di esclusione reciproca. È anche possibile impostare e recuperare informazioni generali sul profilo. Per accedere a tutte le funzionalità dell'oggetto profilo, è necessario usare [**IWMProfile3,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)che eredita da **IWMProfile** e [**IWMProfile2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)

**IWMProfile** è accessibile anche tramite l'oggetto reader, in cui è possibile usarlo per ottenere informazioni sui flussi di un file caricato nel lettore. Quando si accede **a IWMProfile** dal lettore, è possibile apportare modifiche al profilo, ma nessuna delle modifiche può essere salvata nel file. È spesso utile usare il profilo di un file esistente come base di un nuovo profilo. Il lettore sincrono supporta **IWMProfile** nello stesso modo del lettore.

Le informazioni sul profilo ottenute tramite il lettore o il lettore sincrono non provengono da un file con estensione prx. Il lettore usa le informazioni nel file ASF per assemblare le configurazioni del flusso. Alcune informazioni sul profilo, ad esempio il nome e la descrizione, non sono quindi disponibili tramite il lettore.

Esistono diversi modi per ottenere un puntatore a **un'interfaccia IWMProfile.** Il gestore di profili dispone di metodi per creare un nuovo profilo e accedere ai profili esistenti. Tutti questi metodi impostano un **puntatore IWMProfile.** Durante la lettura di un file, è possibile ottenere un puntatore a **IWMProfile** chiamando il **metodo QueryInterface** di qualsiasi interfaccia del lettore. Analogamente, qualsiasi interfaccia dell'oggetto reader sincrono può ottenere un puntatore con una chiamata a **QueryInterface**[**IWMProfile3.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)

## <a name="members"></a>Membri

**L'interfaccia IWMProfile** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMProfile** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWMProfile** include questi metodi.



| Metodo                                                                  | Descrizione                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | Aggiunge un oggetto di esclusione reciproca al profilo.<br/>                                   |
| [**AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | Aggiunge un flusso al profilo.<br/>                                                    |
| [**CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Crea un oggetto di esclusione reciproca per il profilo.<br/>                               |
| [**CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | Crea un oggetto di configurazione del flusso per il profilo.<br/>                           |
| [**GetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | Recupera la descrizione del profilo.<br/>                                        |
| [**GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Recupera un oggetto di esclusione reciproca dal profilo.<br/>                            |
| [**GetMutualExclusionCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | Recupera il numero di oggetti di esclusione reciproca nel profilo.<br/>                 |
| [**GetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | Recupera il nome del profilo.<br/>                                               |
| [**Getstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | Recupera un flusso, utilizzando un numero di indice, dal profilo.<br/>                     |
| [**GetStreamByNumber**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | Recupera un flusso, usando il numero del flusso, dal profilo.<br/>            |
| [**GetStreamCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | Recupera il numero di flussi nel profilo.<br/>                                  |
| [**GetVersion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | Recupera il numero di versione di Microsoft Servizi Windows Media nel profilo.<br/> |
| [**ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | Consente di includere nel profilo le modifiche apportate a una configurazione del flusso.<br/>    |
| [**RemoveMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | Rimuove un oggetto di esclusione reciproca dal profilo.<br/>                              |
| [**RemoveStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | Rimuove un flusso dal profilo.<br/>                                               |
| [**RemoveStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | Rimuove un flusso dal profilo.<br/>                                               |
| [**SetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | Specifica la descrizione del profilo.<br/>                                        |
| [**SetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | Specifica il nome del profilo.<br/>                                               |



 

Per informazioni sulle interfacce che è possibile ottenere usando il metodo QueryInterface di questa interfaccia, vedere l'argomento relativo all'oggetto in cui è implementata questa interfaccia.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](interfaces.md)
</dt> <dt>

[**Interfaccia IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Oggetto Gestione profili**](profile-manager-object.md)
</dt> <dt>

[**Oggetto Lettore**](reader-object.md)
</dt> <dt>

[**Oggetto lettore sincrono**](synchronous-reader-object.md)
</dt> <dt>

[**Uso dei profili**](working-with-profiles.md)
</dt> </dl>

 

