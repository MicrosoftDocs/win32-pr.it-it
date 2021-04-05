---
title: Dimensioni dell'indice
description: Dimensioni dell'indice
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cd9e59c23376a7aa201673ef71743c8a192b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711584"
---
# <a name="index-size"></a>Dimensioni dell'indice

Ogni file AVI usa un indice di una dimensione specificata per individuare i blocchi di dati audio e video all'interno del file. Una voce nell'indice individua un fotogramma video o un buffer audio della forma d'onda. Di conseguenza, il valore della dimensione dell'indice imposta indirettamente il limite superiore per il numero di frame che possono essere acquisiti in un file.

È possibile recuperare le dimensioni correnti degli indici usando il messaggio di [**installazione della \_ sequenza WM Cap \_ get \_ \_**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). La dimensione dell'indice corrente viene archiviata nel membro **dwIndexSize** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . È possibile specificare una nuova dimensione di indice come valore di **dwIndexSize** , quindi inviare la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**di \_ \_ installazione della \_ sequenza \_ di set di WM Cap**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). La dimensione dell'indice predefinita è 34.952 voci (che consentono 32K frame e un numero proporzionale di buffer audio).

 

 




