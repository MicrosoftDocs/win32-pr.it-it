---
title: Informazioni sul API di accesso al dispositivo
description: Il API di accesso al dispositivo è per gli sviluppatori C++ che creano un'app di Windows Store per interagire con dispositivi specializzati in Windows 8.
ms.assetid: DDF115A2-A811-450A-80F7-AAFB0EEA4037
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 08d603e74ff33250bbc5a65e440fc47a0103cd6eb996badf94dbdc51b6b2d3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755021"
---
# <a name="about-the-device-access-api"></a>Informazioni sul API di accesso al dispositivo

Il API di accesso al dispositivo è per gli sviluppatori C++ che creano un'app di Windows Store per interagire con dispositivi specializzati in Windows 8. In questo argomento vengono descritti gli scenari a cui API di accesso al dispositivo si applica. Illustra anche come il API di accesso al dispositivo applica le regole di sicurezza per Windows app dello Store in Windows 8.

- [Abilitazione della funzionalità personalizzata dei dispositivi nelle app Windows Store](#enabling-custom-device-functionality-in-windows-store-device-apps)

## <a name="enabling-custom-device-functionality-in-windows-store-device-apps"></a>Abilitazione della funzionalità personalizzata dei dispositivi nelle app Windows Store

Gli sviluppatori di fornitori di hardware indipendenti (IHV) e OEM possono creare un'app di Windows Store associata al dispositivo e acquisita automaticamente quando il dispositivo viene installato. Questa app, nota come app per Windows Store, può fornire funzionalità univoche del dispositivo.

I dispositivi che non hanno driver di classe predefiniti o API Windows Runtime per la comunicazione con il dispositivo in Windows 8 sono noti come *dispositivi specializzati.* Questi dispositivi potrebbero richiedere un driver personalizzato. Per altre informazioni sui tipi di dispositivi che richiedono driver personalizzati, vedere la guida alla progettazione di app per dispositivi Windows Store per dispositivi specializzati.

L'app per dispositivi Windows Store per un dispositivo specializzato che deve comunicare con il driver personalizzato di un dispositivo non può usare API Microsoft Win32 come [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) e [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) per inviare IOCTL al dispositivo. L'ambiente di sicurezza con restrizioni in cui vengono eseguite le app per dispositivi Windows Store richiede l'uso del API di accesso al dispositivo per comunicare con il driver personalizzato da un'app Windows Store.

Lo sviluppatore di un dispositivo personalizzato limita l'accesso alle applicazioni approvate con privilegi. Ad esempio, il produttore di un dispositivo lettore multimediale potrebbe volere che gli utenti riproducino musica solo tramite l'app di musica fornita da IHV e impedisci all'app concorrente di sincronizzare i file multimediali dal dispositivo. Quando si compila il driver di dispositivo, si imposta una proprietà nel file di informazioni (INF) per specificare che solo le app con privilegi possono accedere al dispositivo. I metadati nel dispositivo stesso specificano gli ID pacchetto per il set di app approvate. Per altri dettagli sul processo di impostazione di questi metadati nel dispositivo, vedi App per dispositivi [UWP](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) per dispositivi interni.

## <a name="related-topics"></a>Argomenti correlati

[Esempio di accesso ai driver](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)personalizzati, app per dispositivi [UWP per dispositivi interni,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Hardware Dev Center](/windows-hardware/drivers/)