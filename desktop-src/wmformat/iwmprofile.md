---
title: Interfaccia IWMProfile
description: L'interfaccia IWMProfile è l'interfaccia principale per un oggetto profilo.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- Formato Windows Media Interface IWMProfile
- Interfaccia IWMProfile-formato Windows Media, descritto
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
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "106300672"
---
# <a name="iwmprofile-interface"></a>Interfaccia IWMProfile

L'interfaccia **IWMProfile** è l'interfaccia principale per un oggetto [*profilo*](wmformat-glossary.md) . Un oggetto profilo viene usato per configurare i profili personalizzati. È possibile usare **IWMProfile** per creare, eliminare o modificare oggetti di configurazione del flusso e oggetti di esclusione reciproca. È inoltre possibile impostare e recuperare informazioni generali sul profilo. Per accedere a tutte le funzionalità dell'oggetto profilo, è necessario usare [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), che eredita da **IWMProfile** e [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).

**IWMProfile** è accessibile anche tramite l'oggetto Reader, in cui è possibile usarlo per ottenere informazioni sui flussi di un file caricato nel lettore. Quando si accede a **IWMProfile** dal lettore, è possibile apportare modifiche al profilo, ma nessuna delle modifiche può essere salvata nel file. Spesso è utile usare il profilo di un file esistente come base di un nuovo profilo. Il lettore sincrono supporta **IWMProfile** in modo analogo al lettore.

Le informazioni sul profilo ottenute tramite il Reader o il lettore sincrono non provengono da un file con estensione prx. Il lettore utilizza le informazioni nel file ASF per assemblare le configurazioni di flusso. Pertanto, alcune informazioni sul profilo, come il nome e la descrizione, non sono disponibili tramite il lettore.

Esistono diversi modi per ottenere un puntatore a un'interfaccia **IWMProfile** . Gestione profili dispone di metodi per creare un nuovo profilo e per accedere ai profili esistenti. Tutti questi metodi impostano un puntatore **IWMProfile** . Quando si legge un file, è possibile ottenere un puntatore a **IWMProfile** chiamando il metodo **QueryInterface** di qualsiasi interfaccia Reader. Analogamente, qualsiasi interfaccia dell'oggetto Reader sincrono può ottenere un puntatore con una chiamata a **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).

## <a name="members"></a>Membri

L'interfaccia **IWMProfile** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMProfile** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMProfile** dispone di questi metodi.



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
| [**GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | Recupera un flusso, usando un numero di indice, dal profilo.<br/>                     |
| [**GetStreamByNumber**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | Recupera un flusso, usando il numero del flusso, dal profilo.<br/>            |
| [**GetStreamCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | Recupera il numero di flussi nel profilo.<br/>                                  |
| [**GetVersion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | Recupera il numero di versione di servizi multimediali di Microsoft Windows nel profilo.<br/> |
| [**ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | Consente di includere nel profilo le modifiche apportate a una configurazione del flusso.<br/>    |
| [**RemoveMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | Rimuove un oggetto di esclusione reciproca dal profilo.<br/>                              |
| [**RemoveStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | Rimuove un flusso dal profilo.<br/>                                               |
| [**RemoveStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | Rimuove un flusso dal profilo.<br/>                                               |
| [**SetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | Specifica la descrizione del profilo.<br/>                                        |
| [**SetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | Specifica il nome del profilo.<br/>                                               |



 

Per informazioni sulle interfacce che è possibile ottenere usando il metodo QueryInterface di questa interfaccia, vedere l'argomento relativo all'oggetto su cui è implementata questa interfaccia.

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

[**Utilizzo dei profili**](working-with-profiles.md)
</dt> </dl>

 

