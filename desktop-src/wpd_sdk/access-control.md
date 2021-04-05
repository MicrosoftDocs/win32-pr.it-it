---
description: Controllo di accesso
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Controllo di accesso (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884917"
---
# <a name="access-control-wpd-api"></a>Controllo di accesso (API WPD)

Il Windows Driver Model (WDM) supporta la restrizione dell'accesso ai dispositivi tramite elenchi di controllo di accesso (ACL) nei nodi del dispositivo Plug and Play (PnP). Ciò significa che i fornitori e gli amministratori di rete possono limitare l'accesso a qualsiasi tipo di dispositivo. Quando un'applicazione apre un handle per un driver chiamando [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), il gestore di i/O del driver verifica se l'utente specificato ha l'accesso richiesto e, in modo analogo, verifica l'accesso quando IOCTL vengono inviati al driver da tale handle.

Un amministratore di rete può, ad esempio, limitare l'accesso in sola lettura ai dispositivi portatili da parte degli utenti guest, sebbene possano concedere agli utenti autenticati l'accesso in lettura/scrittura. In questo caso, significa che se un Guest ha emesso un comando WPD che richiede l'accesso in lettura/scrittura (ad esempio delete Object); si verificherà un errore di accesso negato, mentre se un utente autenticato ha emesso lo stesso comando, avrà esito positivo.

Il Criteri di gruppo voci per il controllo dell'accesso all'archiviazione rimovibile e ai dispositivi portatili non è in realtà un modo semplice per gli amministratori di applicare gli ACL del nodo del dispositivo PnP a un'intera classe di dispositivi alla volta (ad esempio, applicando l'accesso in scrittura per negare i dispositivi portatili) Criteri di gruppo modificare gli ACL di tutti i dispositivi WPD per negare l'accesso in scrittura.

## <a name="io-control-codes-in-wpd"></a>Codici di controllo di I/O in WPD

Le applicazioni WPD comunicano con i driver aprendo gli handle del dispositivo e inviando I codici di controllo di I/O (IOCTL). Queste IOCTL sono costituite da quattro sezioni:

1.  Tipo di dispositivo
2.  Codice funzione
3.  Buffer (metodo)
4.  Tipo di accesso

La quarta sezione, il tipo di accesso, specifica il requisito di accesso specifico per il comando specificato. Il gestore di I/O del driver usa questi dati per eseguire il controllo dell'elenco di controllo di accesso (ACL).

Quindi, se un IOCTL è stato definito come:


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



Il gestore di I/O del driver controlla che il proprietario dell'handle di dispositivo disponga dell'accesso in lettura al dispositivo quando viene inviato questo messaggio.

E, se un IOCTL è stato definito come:


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



Il gestore di I/O del driver controlla che il proprietario dell'handle di dispositivo disponga dell'accesso in lettura/scrittura al dispositivo quando viene inviato questo messaggio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica dell'applicazione**](application-overview.md)
</dt> <dt>

[**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



