---
title: Connessione Web Desktop remoto
description: Connessione Web Desktop remoto è un'applicazione Web costituita da un controllo ActiveX e da una pagina di connessione di esempio.
ms.assetid: f9d252b0-205a-47df-9eca-d5744c09e079
ms.tgt_platform: multiple
keywords:
- Connessione Web Desktop remoto Servizi Desktop remoto
- Servizi Desktop remoto di Remote Desktop Protocol (RDP), Connessione Web Desktop remoto Panoramica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bb1e8f562e3e5c47c6050f550fe3c7090446be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300042"
---
# <a name="remote-desktop-web-connection"></a>Connessione Web Desktop remoto

Connessione Web Desktop remoto è un'applicazione Web costituita da un controllo ActiveX e da una pagina di connessione di esempio. Quando si distribuisce Connessione Web Desktop remoto in un server Web, è possibile fornire la connettività client ai server di host sessione Desktop remoto (host sessione Desktop remoto) e ad altri computer che utilizzano Internet Explorer e TCP/IP.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md)
</dt> <dd>

Elenca i requisiti per un Connessione Web Desktop remoto.

</dd> <dt>

[Canali virtuali tramite script](scriptable-virtual-channels.md)
</dt> <dd>

Vengono descritte le modifiche apportate al modello di programmazione per l'implementazione di applicazioni di canale virtuale fornite dal Client avanzato di Servizi terminal (TSAC).

</dd> </dl>

Il materiale di riferimento per Connessione Web Desktop remoto è incluso nella sezione [connessione Web Desktop remoto Reference](remote-desktop-web-connection-reference.md) .

Per altre informazioni, vedere gli argomenti seguenti:

-   [Implementazione di canali virtuali tramite script con Connessione Web Desktop remoto](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
-   [Incorporamento del controllo ActiveX Desktop remoto in una pagina Web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
-   [Download e utilizzo del controllo ActiveX Desktop remoto](/previous-versions//aa380808(v=vs.85))
-   [Uso del controllo ActiveX Desktop remoto con i canali virtuali](using-the-remote-desktop-activex-control-with-virtual-channels.md)
-   [Fornire la sicurezza del client RDP](providing-for-rdp-client-security.md)
-   [Disabilitazione delle funzionalità di Servizi Desktop remoto](disabling-terminal-services-features.md)

## <a name="installing-remote-desktop-web-connection"></a>Installazione di Connessione Web Desktop remoto

La procedura seguente consente di installare il controllo ActiveX Desktop remoto e la pagina Web di esempio nella directory% SystemRoot% \\ Web \\ nella tsweb. Condividono la pagina Web nella directory nella TSWeb del server, ad esempio, in https://*MyServer*/tsweb. Il controllo (Msrdp. ocx) e il codice Connessione Web Desktop remoto si trovano in Msrdp.cab.

**Per installare Connessione Web Desktop remoto**

1.  Nell'elemento Installazione applicazioni nel pannello di controllo, in installazione componenti di Windows, installare Microsoft Internet Information Services (IIS).
2.  Installare il sottocomponente servizio World Wide Web di IIS.
3.  Installare il sottocomponente Connessione Web Desktop remoto di World Wide Web servizio.

Per una descrizione della pagina Web inclusa con l'installazione di Connessione Web Desktop remoto, vedere [la pagina Web di esempio inclusa nel controllo ActiveX Desktop remoto](sample-web-page-included-with-the-remote-desktop-activex-control.md).

 

 