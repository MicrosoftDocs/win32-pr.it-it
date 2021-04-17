---
title: Provider di servizi ADSI
description: In questo argomento viene fornita una panoramica dei provider di servizi ADSI disponibili nel server.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, provider di servizi
- ADSI provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44ba4ebc63338bfb38d2b9d5da1f46e51b31aa8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300421"
---
# <a name="adsi-service-providers"></a>Provider di servizi ADSI

ADSI include i provider di servizi elencati nella tabella seguente.



| Provider di servizi | Descrizione                                                                                | Per ulteriori informazioni                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| LDAP<br/>  | Implementazione dello spazio dei nomi compatibile con il protocollo Lightweight Directory Access.<br/> | [Provider LDAP ADSI](adsi-ldap-provider.md)<br/>   |
| WinNT<br/> | Implementazione dello spazio dei nomi compatibile con Windows.<br/>                               | [Provider ADSI WinNT](adsi-winnt-provider.md)<br/> |



 

Altri provider di servizi sono inclusi come parte di prodotti diversi da ADSI. Di seguito sono riportati i provider di servizi ADSI implementati da Microsoft.



| Provider di servizi | Per ulteriori informazioni                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| IIS<br/>   | [Architettura del provider ADSI IIS](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))<br/> |



 

I metodi e i metodi di proprietà esposti dalle interfacce ADSI non sono supportati da tutti i provider di servizi. Poiché i diversi servizi directory variano a seconda dei tipi di oggetti e proprietà archiviati, usano protocolli diversi e l'autenticazione, ADSI è progettato per funzionare senza interruzioni con i provider di servizi supportati. Sono pertanto disponibili interfacce, metodi e metodi di proprietà che funzionano con un provider di servizi, ad esempio LDAP, che potrebbero non funzionare in un altro, ad esempio WinNT.

In questa sezione sono contenute informazioni specifiche del provider, ad esempio il formato ADsPath, un elenco di oggetti ADSI utilizzati per il provider di servizi e informazioni sul tipo di dati e sulla sintassi per i provider di servizi inclusi in ADSI. È inoltre disponibile una descrizione riepilogativa delle interfacce ADSI supportate da ogni provider incluso in ADSI.

In ADSI i provider diversi sono associati a DLL diverse. Il provider LDAP è associato a Adsldp.dll, Adsldpc.dll e Adsmsext.dll. Il provider WinNT è associato a Adsnt.dll. Il provider del ROUTER è associato a Activeds.dll.

> [!Note]  
> Non presupporre che i provider ADSI predefiniti siano thread-safe. Gli sviluppatori di applicazioni multithreading devono coordinare l'accesso tra thread attraverso l'uso corretto di oggetti di sincronizzazione, ad esempio semafori, mutex, sezioni critiche e così via.

 

Per ulteriori informazioni sui provider di servizi ADSI, vedere la pagina relativa al supporto del router e del provider [ADSI](adsi-router.md) per [le interfacce ADSI](provider-support-of-adsi-interfaces.md).

 

