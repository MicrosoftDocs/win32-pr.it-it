---
title: Informazioni sull'API di accesso ai dispositivi
description: L'API di accesso ai dispositivi è destinata agli sviluppatori C++ che creano un'app di Windows Store per interagire con dispositivi specializzati in Windows 8.
ms.assetid: DDF115A2-A811-450A-80F7-AAFB0EEA4037
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 213c7ecc618e4b183ee879d23db3b2c0eca35397
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104339595"
---
# <a name="about-the-device-access-api"></a>Informazioni sull'API di accesso ai dispositivi

L'API di accesso ai dispositivi è destinata agli sviluppatori C++ che creano un'app di Windows Store per interagire con dispositivi specializzati in Windows 8. Questo argomento descrive gli scenari a cui si applica l'API di accesso ai dispositivi. Viene inoltre illustrato come l'API di accesso ai dispositivi applica le regole di sicurezza per le applicazioni Windows Store in Windows 8.

- [Abilitazione della funzionalità di dispositivo personalizzata nelle app per dispositivi Windows Store](#enabling-custom-device-functionality-in-windows-store-device-apps)

## <a name="enabling-custom-device-functionality-in-windows-store-device-apps"></a>Abilitazione della funzionalità di dispositivo personalizzata nelle app per dispositivi Windows Store

Gli sviluppatori di fornitori di hardware indipendenti (IHV) e OEM possono compilare un'app di Windows Store abbinata al dispositivo e acquisita automaticamente al momento dell'installazione del dispositivo. Questa app, nota come app per dispositivi Windows Store, può fornire funzionalità univoche per i dispositivi.

I dispositivi che non dispongono di driver di classe predefiniti o API Windows Runtime per la comunicazione con il dispositivo in Windows 8 sono noti come *dispositivi specializzati*. Questi dispositivi potrebbero richiedere un driver personalizzato. Per altre informazioni sui tipi di dispositivi che richiedono driver personalizzati, vedere la guida alla progettazione di app per dispositivi Windows Store per i dispositivi specializzati.

L'app per dispositivi Windows Store per un dispositivo specializzato che deve comunicare con il driver personalizzato di un dispositivo non può usare API Microsoft Win32 come [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) e [**CREATEFILE**](/windows/win32/api/fileapi/nf-fileapi-createfilea) per inviare IOCTL al dispositivo. L'ambiente di sicurezza con restrizioni in cui vengono eseguite le app per dispositivi Windows Store richiede l'uso dell'API di accesso ai dispositivi per comunicare con il driver personalizzato da un'app di Windows Store.

Lo sviluppatore di un dispositivo personalizzato limita l'accesso alle applicazioni con privilegi approvate. Ad esempio, il produttore di un dispositivo Media Player potrebbe volere che gli utenti riproducano musica solo tramite l'app per la musica fornita da IHV e impediscano la sincronizzazione dei supporti dal dispositivo da parte dell'app di un concorrente. Quando si compila il driver di dispositivo, si imposta una proprietà nel collegamento informazioni (INF) per specificare che solo le app con privilegi possono accedere al dispositivo. I metadati nel dispositivo stesso specificano gli ID del pacchetto per il set di app approvate. Per altri dettagli sul processo di impostazione di questi metadati nel dispositivo, vedere [app per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) .

## <a name="related-topics"></a>Argomenti correlati

[Esempio di accesso ai driver personalizzato](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [app per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [hardware Dev Center](/windows-hardware/drivers/)