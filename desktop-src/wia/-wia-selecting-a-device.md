---
description: Quando un'applicazione si connette a un dispositivo hardware Windows Image Acquisition (WIA), WIA crea una struttura ad albero di elementi (un albero gerarchico di interfacce IWiaItem o IWiaItem2) che rappresenta il dispositivo e le relative immagini, cartelle e letti di scansione.
ms.assetid: 2a7bcfd4-4075-48a4-9eff-5210b9a635e3
title: Selezione di un dispositivo (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a2eab41016397f6505e60efcbf78d1fdf82499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879314"
---
# <a name="selecting-a-device-wia"></a>Selezione di un dispositivo (WIA)

Quando un'applicazione si connette a un dispositivo hardware Windows Image Acquisition (WIA), WIA crea una struttura ad albero di elementi (un albero gerarchico di interfacce [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) ) che rappresenta il dispositivo e le relative immagini, cartelle e letti di scansione. Un'applicazione può selezionare e connettersi a un dispositivo senza input utente oppure visualizzare una finestra di dialogo che consente a un utente di selezionare un dispositivo.

-   [Selezione di un dispositivo senza l'interfaccia utente](#selecting-a-device-without-the-ui)
-   [Selezione di un dispositivo con l'interfaccia utente](#selecting-a-device-with-the-ui)

## <a name="selecting-a-device-without-the-ui"></a>Selezione di un dispositivo senza l'interfaccia utente

Per selezionare e connettersi a un dispositivo hardware WIA, attenersi alla procedura riportata di seguito.

-   Chiamare [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per recuperare un puntatore all'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) .
-   Usare il metodo [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) dell'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) per ottenere un puntatore all'interfaccia [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . Per istruzioni su come enumerare i dispositivi, vedere [enumerazione dei dispositivi di sistema](-wia-enumerating-system-devices.md).
-   Usare l'interfaccia [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) per ottenere i puntatori dell'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) per ogni dispositivo WIA enumerato.
-   Usare l'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) per esaminare le proprietà delle informazioni sul dispositivo di ogni dispositivo e salvare la \_ Proprietà WIA DIP \_ dev \_ ID dal dispositivo desiderato.
-   Usare la proprietà DeviceID con il metodo [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) nell'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) per creare un oggetto dispositivo WIA. Il metodo **IWiaDevMgr:: CreateDevice** fornisce all'applicazione il puntatore all'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) dell'elemento radice del dispositivo specificato.

Per un esempio di come eseguire questa operazione in un'applicazione, vedere [creazione di un dispositivo](-wia-creating-a-device.md) nella sezione dell'esercitazione di questa guida.

## <a name="selecting-a-device-with-the-ui"></a>Selezione di un dispositivo con l'interfaccia utente

Dopo aver recuperato un puntatore a [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), un'applicazione può consentire a un utente di selezionare un dispositivo ignorando il resto dei passaggi precedenti e chiamando [**IWiaDevMgr:: SelectDeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg). **IWiaDevMgr:: SelectDeviceDlg** Visualizza una finestra di dialogo in cui l'utente può selezionare un dispositivo WIA.

È consigliabile che le applicazioni rendano disponibili la selezione del dispositivo e dell'immagine tramite una voce di menu denominata **da scanner** nel menu **file** .

 

 
