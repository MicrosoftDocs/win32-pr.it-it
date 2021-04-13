---
title: Come usare l'API di accesso ai dispositivi
description: Questo argomento contiene le attività e le considerazioni di progettazione per l'uso dell'API di accesso ai dispositivi.
ms.assetid: 8D951EB5-4AFB-4051-8F1F-30F847F1A757
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 29c4812c559b691a896fb5bb9da39064bf3c8614
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104399890"
---
# <a name="how-to-use-the-device-access-api"></a>Come usare l'API di accesso ai dispositivi

Questo argomento contiene le attività e le considerazioni di progettazione per l'uso dell'API di accesso ai dispositivi.

## <a name="steps"></a>Passaggi

| Argomento | Descrizione |
|---|---|
| [Considerazioni di progettazione per i dispositivi personalizzati](design.md)<br/> | Questo argomento descrive le considerazioni di progettazione che consentono di determinare se il dispositivo necessita di un driver personalizzato.<br/> |
| [Implementare l'oggetto di accesso al dispositivo](create-the-device-access-object.md)<br/> | Questo argomento illustra come creare un'istanza dell'oggetto di accesso al dispositivo e usarlo per accedere a un dispositivo. <br/>  |
| [Dichiarazione della funzionalità del dispositivo](declaring-the-device-capability.md)<br/> | In questo argomento viene illustrato come dichiarare il GUID della funzionalità del dispositivo.<br/> |
| [Registrare l'interfaccia del dispositivo come limitata alle app con privilegi](register-the-device-interface-class-as-privileged.md)<br/> | In questo argomento viene illustrato come aggiungere la proprietà **Restricted** che indica che solo le app con privilegi possono accedere a una classe di interfaccia del dispositivo.<br/> |
| [Creare un'estensione di Windows Runtime](create-a-windows-runtime-extension.md)<br/> | È possibile creare un componente Windows Runtime per eseguire il wrapping del componente che accede al driver. È quindi possibile scrivere un'app per dispositivi Windows Store per il dispositivo in C# o JavaScript.<br/> |

## <a name="additional-resources"></a>Risorse aggiuntive

- L' [esempio di accesso ai driver personalizzati](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) illustra come usare le API di accesso ai dispositivi per accedere a un driver personalizzato da un'app per dispositivi Windows Store.
- [App per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) fornisce risorse per ulteriori informazioni su come progettare e sviluppare app per dispositivi Windows Store per dispositivi specializzati.
- [Hardware Dev Center](/windows-hardware/drivers/) fornisce le risorse generali per le attività di sviluppo di app per dispositivi Windows Store comuni a tutti i tipi di dispositivi.
