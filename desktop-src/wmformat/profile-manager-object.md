---
title: Oggetto Gestione profili
description: Oggetto Gestione profili
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- Windows Media Format SDK, oggetti di gestione profili
- Advanced Systems Format (ASF), oggetti di gestione profili
- ASF (Advanced Systems Format),oggetti di gestione profili
- oggetti, oggetti di gestione profili
- profili, oggetti
- profili, oggetti di gestione profili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce272067e98f787d5136cacc0a2d02f474264f14f14aa785b28162945ef1b41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084648"
---
# <a name="profile-manager-object"></a>Oggetto Gestione profili

Un profilo è un set di parametri multimediali usati per creare un file ASF. L'oggetto gestione profili crea oggetti profilo per la modifica. Gli oggetti profilo possono essere creati senza dati o compilati da dati di profilo esistenti. L'oggetto profile manager fornisce anche metodi per enumerare i codec supportati ed eseguire query su tali codec per ottenere informazioni.

L'oggetto di gestione profili viene creato dalla [**funzione WMCreateProfileManager,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) che imposta un puntatore a [**un'interfaccia IWMProfileManager.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) Le altre interfacce dell'oggetto di gestione dei profili possono essere ottenute chiamando il **metodo QueryInterface.**

Le interfacce seguenti sono supportate dall'oggetto di gestione dei profili.



| Interfaccia                                                      | Descrizione                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | Recupera informazioni sui codec supportati e i relativi formati.                                                                              |
| [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | Recupera i nomi dei codec supportati e le descrizioni dei relativi formati. Eredita tutti i metodi di **IWMCodecInfo.**          |
| [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | Recupera le proprietà del codec ed esegue query sui codec per le funzionalità supportate. Eredita tutti i metodi di **IWMCodecInfo** e **IWMCodecInfo2.** |
| [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | Crea nuovi profili, carica i profili esistenti e salva i profili personalizzati.                                                                    |
| [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | Controlla la versione dei profili di sistema enumerati da Gestione profili. Eredita tutti i metodi di **IWMProfileManager.**             |
| [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | Controlla la lingua dei profili di sistema analizzati da Gestione profili.                                                                  |



 

## <a name="remarks"></a>Commenti

Quando viene creato un oggetto di gestione profili, vengono analizzati tutti i profili di sistema, operazione che può richiedere alcuni secondi. La creazione e il rilascio di una gestione profili ogni volta che è necessario usarlo influiranno negativamente sulle prestazioni. È consigliabile creare una gestione profili una sola volta nell'applicazione e rilasciarla solo quando non è più necessario usarla.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto Profile**](profile-object.md)
</dt> <dt>

[**Profiles**](profiles.md)
</dt> </dl>

 

 




