---
title: Provider di servizi ADSI
description: In questo argomento viene fornita una panoramica dei provider di servizi ADSI disponibili nel server.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , provider di servizi
- Provider di servizi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66b90aad4e9fa1a6cf6a2229910257f018a411aa7b11b9accca6fcf96dce39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962208"
---
# <a name="adsi-service-providers"></a>Provider di servizi ADSI

ADSI include i provider di servizi elencati nella tabella seguente.



| Provider di servizi | Descrizione                                                                                | Per ulteriori informazioni                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| LDAP<br/>  | Implementazione dello spazio dei nomi compatibile con Lightweight Directory Access Protocol.<br/> | [ADSI LDAP Provider](adsi-ldap-provider.md)<br/>   |
| Winnt<br/> | Implementazione dello spazio dei nomi compatibile con Windows.<br/>                               | [ADSI WinNT Provider](adsi-winnt-provider.md)<br/> |



 

Altri provider di servizi sono inclusi come parte di prodotti diversi da ADSI. Di seguito sono riportati i provider di servizi ADSI implementati da Microsoft.



| Provider di servizi | Per ulteriori informazioni                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| IIS<br/>   | [Architettura del provider ADSI IIS](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))<br/> |



 

I metodi e i metodi delle proprietà esposti dalle interfacce ADSI non sono supportati da tutti i provider di servizi. Poiché i diversi servizi directory variano nei tipi di oggetti e proprietà archiviati, usano protocolli e autenticazione diversi, ADSI è progettato per funzionare senza problemi con i provider di servizi supportati. Di conseguenza, esistono interfacce, metodi e metodi di proprietà che funzionano con un provider di servizi, ad esempio LDAP, che potrebbero non funzionare in un altro, ad esempio WinNT.

Questa sezione contiene informazioni specifiche del provider, ad esempio il formato ADsPath, un elenco di oggetti ADSI utilizzati per tale provider di servizi e informazioni sul tipo di dati e sulla sintassi per i provider di servizi inclusi in ADSI. È inoltre disponibile una descrizione di riepilogo delle interfacce ADSI supportate da ogni provider incluso in ADSI.

In ADSI provider diversi sono associati a DLL diverse. Il provider LDAP è associato a Adsldp.dll, Adsldpc.dll e Adsmsext.dll. Il provider WinNT è associato a Adsnt.dll. Il provider ROUTER è associato a Activeds.dll.

> [!Note]  
> Non presupporre che i provider ADSI predefiniti siano thread-safe. Gli sviluppatori di applicazioni multithreading devono coordinare l'accesso tra thread tramite l'uso corretto di oggetti di sincronizzazione, ad esempio semafori, mutex, sezioni critiche e così via.

 

Per altre informazioni sui provider di servizi ADSI, vedere Supporto di router e provider [ADSI](adsi-router.md) [per le interfacce ADSI.](provider-support-of-adsi-interfaces.md)

 

