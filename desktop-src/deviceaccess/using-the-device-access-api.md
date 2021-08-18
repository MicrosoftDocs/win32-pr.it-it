---
title: Come usare il API di accesso al dispositivo
description: Questo argomento contiene attività e considerazioni di progettazione per l'uso del API di accesso al dispositivo.
ms.assetid: 8D951EB5-4AFB-4051-8F1F-30F847F1A757
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: bd1ddf9d2716cd01ab2db8acb08d2793a6831ffa6f20aa2c75378f72932d992b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635301"
---
# <a name="how-to-use-the-device-access-api"></a>Come usare il API di accesso al dispositivo

Questo argomento contiene attività e considerazioni di progettazione per l'uso del API di accesso al dispositivo.

## <a name="steps"></a>Passaggi

| Argomento | Descrizione |
|---|---|
| [Considerazioni sulla progettazione per i dispositivi personalizzati](design.md)<br/> | In questo argomento vengono descritte le considerazioni di progettazione che consentono di determinare se il dispositivo necessita di un driver personalizzato.<br/> |
| [Implementare l'oggetto Device Access](create-the-device-access-object.md)<br/> | Questo argomento illustra come creare un'istanza dell'oggetto di accesso al dispositivo e usarlo per accedere a un dispositivo. <br/>  |
| [Dichiarazione della funzionalità del dispositivo](declaring-the-device-capability.md)<br/> | Questo argomento illustra come dichiarare il GUID della funzionalità di dispositivo.<br/> |
| [Registrare l'interfaccia del dispositivo come limitata alle app con privilegi](register-the-device-interface-class-as-privileged.md)<br/> | Questo argomento illustra come aggiungere la **proprietà Restricted** che indica che solo le app con privilegi possono accedere a una classe di interfaccia del dispositivo.<br/> |
| [Creare un'estensione Windows runtime](create-a-windows-runtime-extension.md)<br/> | È possibile creare un componente Windows runtime per eseguire il wrapping del componente che accede al driver. È quindi possibile scrivere un'app Windows Store per il dispositivo in C# o JavaScript.<br/> |

## <a name="additional-resources"></a>Risorse aggiuntive

- [L'esempio di accesso](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) ai driver personalizzati illustra come usare le API di accesso ai dispositivi per accedere a un driver personalizzato da un'app per Windows Store.
- [Le app per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) forniscono risorse per altre informazioni su come progettare e sviluppare app per dispositivi Windows Store per dispositivi specializzati.
- Il [Hardware Dev Center](/windows-hardware/drivers/) fornisce risorse generali per le Windows di sviluppo di app per dispositivi dello Store comuni a tutti i tipi di dispositivi.
