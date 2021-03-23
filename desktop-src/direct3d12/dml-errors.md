---
title: Gestione degli errori e della rimozione dei dispositivi in DirectML
description: In questo argomento viene illustrato come eseguire il debug della rimozione del dispositivo DirectML e di altre condizioni di errore.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b4567558b8b75685db16796e921f3daf35b849a1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548828"
---
# <a name="handling-errors-and-device-removal-in-directml"></a>Gestione degli errori e della rimozione dei dispositivi in DirectML

## <a name="device-removal"></a>Rimozione del dispositivo

Se si verifica un errore irreversibile, il dispositivo DirectML può entrare nello stato "dispositivo-rimosso". Gli errori irreversibili che provocano la rimozione del dispositivo includono un utilizzo non valido dell'API (per i metodi che non restituiscono un valore [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), errori del driver, errori hardware o condizioni di memoria insufficiente.

Quando un dispositivo DirectML viene rimosso, tutte le chiamate al metodo nel dispositivo e ogni oggetto creato da tale dispositivo diventano no-Ops. Per i metodi che restituiscono un valore [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), viene restituito un codice di errore [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) . È possibile usare il [metodo **IDMLDevice:: GetDeviceRemovedReason**](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) per verificare se il dispositivo DirectML è stato rimosso e per recuperare un codice di errore più dettagliato.

Non è possibile eseguire il ripristino dalla rimozione del dispositivo tranne rilasciando il dispositivo interessato e tutti i relativi elementi figlio, quindi ricreando il dispositivo DirectML da zero.

Il dispositivo-la rimozione del dispositivo Direct3D 12 sottostante causa anche la rimozione del dispositivo DirectML. Non è tuttavia consentito il contrario. Il dispositivo DirectML-la rimozione potrebbe non necessariamente far rimuovere il dispositivo Direct3D 12 sottostante.

## <a name="debugging-directml-device-removal-and-other-errors"></a>Debug del dispositivo DirectML-rimozione e altri errori

La ragione più comune degli errori DirectML è l'utilizzo dell'API non valido. Un utilizzo non valido dell'API potrebbe comportare un codice di errore HRESULT **E_INVALIDARG** o potrebbe causare la rimozione del dispositivo.

Si consiglia di abilitare il livello di [debug DirectML](dml-debug-layer.md) durante lo sviluppo, per intercettare ed eseguire il debug di tali errori. Il livello di debug DirectML esegue una convalida completa dei parametri del metodo e dell'utilizzo delle API e genera messaggi di output di debug che consentono di eseguire il debug.

## <a name="see-also"></a>Vedi anche

* [Uso del livello di debug DirectML](dml-debug-layer.md)
