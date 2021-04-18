---
description: Dopo aver selezionato un'immagine, un'applicazione utilizza l'interfaccia IWiaDataTransfer (per le applicazioni in esecuzione in Windows XP o versioni precedenti) o l'interfaccia IWiaTransfer (per le applicazioni eseguite in Windows Vista o versioni successive) per trasferire i dati immagine dai dispositivi di imaging. Per informazioni dettagliate, vedere Trasferimento di dati di immagine in WIA 1,0 o trasferimento di dati immagine in WIA 2,0.
ms.assetid: cf76e526-d63b-4ee5-ba3c-871f2051a82c
title: Acquisizione di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d062cb370327311ad0c7d4f883344c05bb776f6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312458"
---
# <a name="acquiring-images"></a>Acquisizione di immagini

Dopo aver selezionato un'immagine, un'applicazione utilizza l'interfaccia [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) (per le applicazioni in esecuzione in Windows XP o versioni precedenti) o l'interfaccia [**IWiaTransfer**](-wia-iwiatransfer.md) (per le applicazioni eseguite in Windows Vista o versioni successive) per trasferire i dati immagine dai dispositivi di imaging. Per informazioni dettagliate, vedere [trasferimento di dati di immagine in wia 1,0](-wia-transferring-image-data.md) o [trasferimento di dati immagine in WIA 2,0](-wia-transferring-image-data-in-wia2.md) .

Dopo aver selezionato un dispositivo, un'applicazione usa il metodo [**IWiaItem::D evicedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) dell'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) del dispositivo (elemento radice) per selezionare un'immagine da un dispositivo Windows Image Acquisition (WIA) specificato. Il metodo [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) Visualizza una finestra di dialogo che consente a un utente di selezionare un'immagine da un dispositivo specificato e trasferisce l'immagine in un nome di file selezionato dall'utente. Consente inoltre all'utente di specificare un dispositivo, se necessario. Per altre informazioni, vedere [selezione di un dispositivo](-wia-selecting-a-device.md)

Si noti che non è necessario che un utente selezioni un'immagine usando il metodo sopra riportato. Un'applicazione può ottenere un puntatore a un elemento immagine direttamente dall'albero degli elementi di un dispositivo. Per istruzioni, vedere [esplorazione di un albero degli elementi](-wia-navigating-an-item-tree.md).

Una volta selezionato l'elemento WIA che rappresenta l'immagine desiderata, un'applicazione in esecuzione in Windows XP o versioni precedenti esegue una query sull'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) dell'elemento per un puntatore alla relativa interfaccia [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) . Un'applicazione in esecuzione in Windows Vista o versioni successive esegue una query sull'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) per un puntatore alla relativa interfaccia [**IWiaTransfer**](-wia-iwiatransfer.md) .

L'applicazione può quindi usare i metodi dell'interfaccia [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) (o [**IWiaTransfer**](-wia-iwiatransfer.md)) per trasferire i dati dell'immagine all'applicazione.

Se il dispositivo di imaging è uno scanner, [**IWiaDataTransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)o altri metodi dell'interfaccia [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) , attiva un'operazione di analisi e quindi trasferisce i dati immagine risultanti. Se il dispositivo è una fotocamera, i dati dell'immagine vengono semplicemente trasferiti dalla fotocamera all'applicazione.

 

 



