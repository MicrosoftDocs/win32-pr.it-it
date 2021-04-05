---
title: Chiavi che terminano l'acquisizione
description: Chiavi che terminano l'acquisizione
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Struttura CAPTUREPARMS
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a91d6ee7d07ed36c11cce7e888c9a9710f403cf9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725114"
---
# <a name="keys-ending-capture"></a>Chiavi che terminano l'acquisizione

È possibile consentire all'utente di interrompere una sessione di acquisizione premendo un tasto o una combinazione di tasti dalla tastiera oppure premendo il pulsante destro o sinistro del mouse. Se l'utente interrompe una sessione di acquisizione in tempo reale, il contenuto del file di acquisizione viene ignorato. Se l'utente interrompe una sessione di acquisizione con frame di passaggio, il contenuto del file di acquisizione fino al punto di interruzione dell'acquisizione viene salvato.

È possibile recuperare le impostazioni per interrompere una sessione di acquisizione usando il messaggio [**di \_ \_ installazione della \_ sequenza \_**](wm-cap-get-sequence-setup.md) di acquisizione di WM Cap (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). L'impostazione della sequenza di tasti corrente è archiviata nel membro **vKeyAbort** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . le impostazioni correnti del mouse sono archiviate nei membri **fAbortLeftMouse** e **fAbortRightMouse** . È possibile impostare una nuova combinazione di tasti o sequenze di tasti specificando la combinazione di KeyCode o KeyCode (come nella combinazione di tasti CTRL o MAIUSC) come valore di **vKeyAbort** oppure impostare il pulsante sinistro o destro del mouse come tasto di interruzione specificando il membro **fAbortLeftMouse** o **fAbortRightMouse** . Dopo aver impostato questi membri, inviare la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**di \_ \_ installazione della \_ sequenza \_ del set**](wm-cap-set-sequence-setup.md) di test WM (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). Il valore predefinito di **vKeyAbort** è VK \_ escape. È necessario chiamare la funzione [RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey) prima di specificare una sequenza di tasti che può interrompere una sessione di acquisizione. I valori predefiniti di **fAbortLeftMouse** e **fAbortRightMouse** sono **true**.

 

 