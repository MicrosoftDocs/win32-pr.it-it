---
title: Oggetto Gestione profili
description: Oggetto Gestione profili
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- Windows Media Format SDK, oggetti Profile Manager
- ASF (Advanced Systems Format), oggetti Profile Manager
- ASF (Advanced Systems Format), oggetti Profile Manager
- oggetti, oggetti di gestione profili
- profili, oggetti
- profili, oggetti Profile Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299517"
---
# <a name="profile-manager-object"></a>Oggetto Gestione profili

Un profilo è un set di parametri multimediali utilizzati per creare un file ASF. L'oggetto Gestione profili crea oggetti profilo per la modifica. È possibile creare oggetti profilo senza dati in essi o compilati da dati di profilo esistenti. L'oggetto Profile Manager fornisce anche metodi per l'enumerazione dei codec supportati e l'esecuzione di query su tali codec per ottenere informazioni.

L'oggetto di gestione dei profili viene creato dalla funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) , che imposta un puntatore a un'interfaccia [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . È possibile ottenere le altre interfacce dell'oggetto Profile Manager chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate dall'oggetto Gestione profili.



| Interfaccia                                                      | Descrizione                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | Recupera le informazioni sui codec supportati e i relativi formati.                                                                              |
| [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | Recupera i nomi dei codec supportati e le descrizioni dei relativi formati. Eredita tutti i metodi di **IWMCodecInfo**.          |
| [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | Recupera le proprietà dei codec e i codec delle query per le funzionalità supportate. Eredita tutti i metodi di **IWMCodecInfo** e **IWMCodecInfo2**. |
| [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | Crea nuovi profili, carica i profili esistenti e salva i profili personalizzati.                                                                    |
| [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | Controlla la versione dei profili di sistema enumerati da Gestione profili. Eredita tutti i metodi di **IWMProfileManager**.             |
| [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | Controlla la lingua dei profili di sistema analizzati da Gestione profili.                                                                  |



 

## <a name="remarks"></a>Commenti

Quando un oggetto di gestione profili viene creato, analizza tutti i profili di sistema, operazione che può richiedere alcuni secondi. La creazione e il rilascio di un gestore profili ogni volta che è necessario utilizzarlo influirà negativamente sulle prestazioni. È necessario creare un gestore profili una volta nell'applicazione e rilasciarlo solo quando non è più necessario utilizzarlo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto profilo**](profile-object.md)
</dt> <dt>

[**Profili**](profiles.md)
</dt> </dl>

 

 




