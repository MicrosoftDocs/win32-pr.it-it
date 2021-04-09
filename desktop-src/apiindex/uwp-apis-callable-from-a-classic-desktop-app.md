---
description: La regola generale è che un'app desktop può chiamare un'API Windows Runtime (WinRT). Tuttavia, alcune API, incluse le API dell'interfaccia utente XAML, richiedono che l'app chiamante disponga di un'identità del pacchetto.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: API WinRT chiamabili da un'app desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9083fbfb16391c626f49b79176fed7a81068c028
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/24/2020
ms.locfileid: "104047587"
---
# <a name="calling-winrt-apis-from-a-desktop-app"></a>Chiamata di API WinRT da un'app desktop

La regola generale è che un'app desktop può chiamare un'API WinRT. Tuttavia, alcune API, incluse le API dell'interfaccia utente XAML, richiedono che l'app chiamante disponga di un'identità del pacchetto. Le app UWP hanno un modello di app ben definito e hanno un'identità del pacchetto. Gli altri tipi di app desktop non includono un modello di app ben definito, né un'identità del pacchetto. Se quindi un'API richiede un'identità del pacchetto, un'app WPF, Windows Form o Win32 non può chiamarla a meno che l'app non [sia stata assemblata in un pacchetto MSIX](/windows/msix/desktop/desktop-to-uwp-root).

## <a name="the-dualapipartition-attribute"></a>Attributo DualApiPartition

Questo è il processo da seguire ogni volta che è presente un particolare WinRT che si vuole chiamare dall'app desktop. Questo processo risponderà alla domanda se l'API può essere chiamata da un'app desktop. Per prima cosa, vedere le informazioni di [riferimento sulle API Windows per Windows Runtime app](/uwp/), trovare l'argomento di riferimento per la classe o l'API membro a cui si è interessati e verificare se l'attributo [**DualApiPartition**](/uwp/api/Windows.Foundation.Metadata.DualApiPartitionAttribute) è elencato nella sezione degli attributi.

## <a name="if-the-dualapipartition-attribute-is-listed"></a>Se l'attributo DualApiPartition è elencato

Se l'attributo DualApiPartition è elencato, l'API non richiede che l'app chiamante disponga di un'identità del pacchetto e che l'API possa essere chiamata da qualsiasi app desktop. [**Windows. Devices. Geolocation. Geolocator**](/uwp/api/Windows.Devices.Geolocation.Geolocator) è un esempio. non è necessario identificare in modo univoco un'app per eseguire le attività di posizione.

## <a name="if-the-dualapipartition-attribute-is-not-listed"></a>Se l'attributo DualApiPartition non è elencato

Se l'attributo DualApiPartition non è elencato, l'API richiede che l'app chiamante disponga di un'identità del pacchetto. Pertanto, un'app WPF, Windows Form o Win32 non è autorizzata a chiamare l'API, a meno che l'app non sia stata convertita in un'app UWP. [**Windows. UI. XAML. Controls. Button**](/uwp/api/Windows.UI.Xaml.Controls.Button) è un esempio.
