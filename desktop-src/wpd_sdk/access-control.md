---
description: Controllo di accesso
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Controllo di accesso (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83caa01b08409afd196ea0507cb47986928a1d947b6ff7907640e4f9bd5b390f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657911"
---
# <a name="access-control-wpd-api"></a>Controllo di accesso (API WPD)

Il Windows Driver Model (WDM) supporta la limitazione dell'accesso ai dispositivi tramite elenchi di controllo di accesso (ACL) nei nodi del dispositivo Plug and Play (PnP). Ciò significa che i fornitori e gli amministratori di rete possono limitare l'accesso a qualsiasi tipo di dispositivo. Quando un'applicazione apre un handle a un driver chiamando [**IPortableDevice::Open,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)gestione I/O del driver verifica se l'utente specificato ha l'accesso necessario e, analogamente, esegue controlli di accesso quando gli IOCTL vengono inviati al driver da tale handle.

Ad esempio, un amministratore di rete potrebbe limitare gli utenti Guest all'accesso in sola lettura per i dispositivi portatili, mentre gli utenti autenticati potrebbero concedere l'accesso in lettura/scrittura agli utenti autenticati. In questo caso, implica che se un guest ha emesso un comando WPD che richiedeva l'accesso in lettura/scrittura (ad esempio Delete Object); l'operazione avrà esito negativo con accesso negato, mentre se un utente autenticato eseguisse lo stesso comando, l'operazione avrebbe esito positivo.

Le voci Criteri di gruppo per controllare l'accesso all'archiviazione rimovibile e ai dispositivi portatili non sono altro che un modo semplice per gli amministratori di applicare gli ACL del nodo del dispositivo PnP a un'intera classe di dispositivi alla volta (ad esempio, l'applicazione del Criteri di gruppo "Nega accesso in scrittura ai dispositivi portatili" regola gli ACL di tutti i dispositivi WPD per negare l'accesso in scrittura).

## <a name="io-control-codes-in-wpd"></a>Codici di controllo I/O in WPD

Le applicazioni WPD comunicano con i driver aprendo handle di dispositivo e inviando codici di controllo I/O (IOCTL). Questi IOCTL sono costituiti da quattro sezioni:

1.  Tipo di dispositivo
2.  Codice funzione
3.  Metodo Buffer
4.  Tipo di accesso

La quarta sezione, Tipo di accesso, specifica il requisito di accesso specifico per il comando specificato. Il gestore di I/O del driver usa questi dati per eseguire il controllo dell'elenco di controllo di accesso (ACL).

Pertanto, se un IOCTL è stato definito come:


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



Il gestore I/O del driver verifica che il proprietario dell'handle del dispositivo abbia accesso in lettura al dispositivo quando viene inviato questo messaggio.

E, se un IOCTL è stato definito come:


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



Il gestore di I/O del driver verifica che il proprietario dell'handle del dispositivo abbia accesso in lettura/scrittura al dispositivo quando viene inviato questo messaggio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica dell'applicazione**](application-overview.md)
</dt> <dt>

[**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



