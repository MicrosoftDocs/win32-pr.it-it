---
title: Allocazione di ID WinEvent
description: Ogni WinEvent deve essere usato solo per uno scopo specifico. L'uso di un evento WinEvent per uno scopo imprevisto può causare conflitti con altre applicazioni o con il sistema operativo, causando l'instabilità delle applicazioni o del sistema operativo.
ms.assetid: 956d6db4-f342-4b11-bfd9-92725284223f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e877c6adcba79870d887e0bdb0d2eb9137d9e04fda4c1cc770414d0dd01f96d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326883"
---
# <a name="allocation-of-winevent-ids"></a>Allocazione di ID WinEvent

Ogni WinEvent deve essere usato solo per uno scopo specifico. L'uso di un evento WinEvent per uno scopo imprevisto può causare conflitti con altre applicazioni o con il sistema operativo, causando l'instabilità delle applicazioni o del sistema operativo.

Microsoft ha definito diverse categorie di WinEvent e, per ogni categoria, ha definito uno o più intervalli di valori da usare come ID WinEvent. L'Community riservato (0xA000, 0xAFFF) è disponibile per le applicazioni che devono definire nuovi Eventi WinEvent. L'uso di valori di questo intervallo consente di ridurre il rischio di collisioni. Tuttavia, gli sviluppatori che creano nuovi eventi WinEvent devono comunque collaborare per evitare conflitti tra le applicazioni.

La tabella seguente illustra le categorie WinEvent e gli intervalli di valori definiti per ogni categoria.



| Category                                                | Intervallo         | Attualmente in uso | Commenti                                                                                        |
|---------------------------------------------------------|---------------|------------------|-------------------------------------------------------------------------------------------------|
| Microsoft Active Accessibility eventi (riservato dal sistema) | 0x0001-0x00FF | 0x0001-0x0020    | ID \_ evento SISTEMA \_ \* EVENTI                                                                     |
| Microsoft Active Accessibility eventi (riservato dal sistema) | 0x4001-0x40FF | 0x4001-0x4007    | ID \_ evento di CONSOLE \_ \* EVENTI                                                                    |
| Automazione interfaccia utente eventi (riservato dal sistema)                  | 0x4E00-0x4EFF | 0x4E20-0x4E33    | Automazione interfaccia utente ID evento                                                                         |
| Automazione interfaccia utente eventi (riservato dal sistema)                  | 0x7500-0x75FF | 0x7530-0x759B    | Automazione interfaccia utente ID evento modificato dalla proprietà                                                        |
| Microsoft Active Accessibility eventi (riservato dal sistema) | 0x8000-0x80FF | 0x8000-0x8015    | ID \_ evento \_ \* DELL'OGGETTO EVENTO                                                                     |
| Riservato OEM                                            | 0x0101-0x01FF | 0x0101-0x0122    | ID evento IAccessible2                                                                          |
| Community Riservati                                      | 0xA000-0xAFFF | Nessuno             | Riservato per i nuovi eventi definiti dalle specifiche accessibility interoperability alliance (AIA) |
| ATOM                                                    | 0xC000-0xFFFF | 0xC000-0xFFFF    | Riservato per gli eventi personalizzati allocati in fase di esecuzione                                                 |



 

Gli argomenti seguenti descrivono gli intervalli WinEvent in modo più dettagliato.

## <a name="microsoft-active-accessibility-and-ui-automation-events"></a>Microsoft Active Accessibility e Automazione interfaccia utente eventi

Cinque intervalli di ID WinEvent sono riservati per l'uso da parte di Microsoft Active Accessibility e Microsoft Automazione interfaccia utente. Il primo intervallo (0x0001— 0x00FF) è riservato agli eventi a livello di sistema, in genere usati per descrivere le situazioni che interessano tutte le applicazioni nel sistema. Il secondo intervallo (0x4001— 0x40FF) è riservato per Windows eventi specifici della console. Il terzo (0x4E00— 0x4EFF) e il quarto intervallo (0x7500— 0x75FF) sono per la reflection di Automazione interfaccia utente eventi. Infine, il quinto intervallo (0x8000— 0x80FF) è per gli eventi a livello di oggetto che riguardano situazioni specifiche degli oggetti all'interno di un'applicazione.

Tutti Microsoft Active Accessibility e Automazione interfaccia utente eventi sono definiti nei file di intestazione WinUser.h e UIAutomationClient.h.

## <a name="oem-reserved-events"></a>Eventi riservati OEM

L'intervallo riservato OEM è aperto a tutti gli utenti che devono usare WinEvents come meccanismo di comunicazione. Gli sviluppatori devono definire e pubblicare definizioni di eventi insieme ai relativi parametri (o anche ai tipi di oggetto associati) per l'elaborazione degli eventi in modo da evitare collisioni accidentali degli ID evento. La specifica IAccessible2 usa parte dell'intervallo riservato OEM.

## <a name="community-reserved-events"></a>Community Eventi riservati

L Community'intervallo riservato è per Gli eventi WinEvent specificati da Accessibility Interoperability Alliance (AIA) per l'uso in tutto il settore. Gli sviluppatori sono fortemente invitati a definire e pubblicare una specifica ufficiale prima di usare i valori di questo intervallo.

## <a name="atom-events"></a>Eventi ATOM

L'intervallo ATOM è riservato agli ID evento allocati in fase di esecuzione tramite l Automazione interfaccia utente API di estendibilità. Non usare i valori dell'intervallo ATOM per altri scopi. [**L'uso della funzione GlobalAddAtom**](/windows/desktop/api/winbase/nf-winbase-globaladdatoma) con un GUID stringa è il metodo consigliato per allocare WinEvents dall'intervallo ATOM.

## <a name="using-values-from-a-reserved-range"></a>Uso di valori da un intervallo riservato

In base alla specifica WinEvent, i valori dell'intervallo Riservato di sistema o qualsiasi altro intervallo non definito non possono essere usati senza rivedere l'SDK. Per i nuovi Eventi WinEvent, le applicazioni devono usare i valori degli intervalli riservati o Community OEM. Prima di usare un nuovo WinEvent, agli sviluppatori è consigliabile condividere le specifiche in modo aperto e ampio e collaborare con Accessibility Interoperability Alliance per definire le specifiche WinEvent.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[Accessibility Interoperability Alliance](https://www.atia.org/)
</dt> </dl>

 

 