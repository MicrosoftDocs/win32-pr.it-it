---
description: In Windows Vista e versioni successive, è possibile utilizzare pseudo-impostazioni locali per testare la localizzabilità delle applicazioni. In questo argomento sono incluse le procedure per l'utilizzo di pseudo-codici.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Utilizzo di pseudo-impostazioni locali per i test di localizzabilità
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: f8c6b435b85a5bef98eff9bf76681096779433e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319473"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a>Utilizzo di pseudo-impostazioni locali per i test di localizzabilità

Le [pseudo-impostazioni locali](pseudo-locales.md) sono incorporate in Windows Vista e versioni successive, in modo che sia possibile accedervi tramite le API NLS (National Language Support). È possibile utilizzare le pseudo-impostazioni locali per testare la [localizzabilità](/windows/uwp/design/globalizing/globalizing-portal) delle applicazioni. In questo argomento sono incluse le procedure per l'utilizzo di pseudo-codici.

> [!NOTE]
> Un'attività che richiede particolare attenzione quando si tratta di pseudo-impostazioni locali li enumera; sia nel codice che nella parte relativa alle opzioni internazionali e della lingua del pannello di controllo. Ulteriori informazioni su più avanti in questo argomento.

I nomi delle pseudo-impostazioni locali sono "query al secondo-ploc", "query al secondo-Besca" e "query al secondo-plocm". A partire da Windows 10, sono disponibili anche le pseudo-impostazioni locali "query al secondo-Latn-x-SH".

## <a name="retrieve-information-about-pseudo-locales"></a>Recuperare informazioni sulle pseudo-impostazioni locali

È possibile usare [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) per recuperare informazioni su pseudo-impostazioni locali. Passare alla funzione il nome delle pseudo-impostazioni locali specifiche. vedere l'elenco dei nomi precedenti. Ad esempio, "query al secondo-plocm" per le pseudo-impostazioni locali con mirroring.

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a>Usare LocaleNameToLCID con pseudo-impostazioni locali

È possibile chiamare la funzione di mapping NLS [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) con il nome di una pseudo-impostazioni locali.

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a>Abilita pseudo-impostazioni locali per l'enumerazione

Nell'applicazione è possibile chiamare [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) per enumerare le impostazioni locali riconosciute dal sistema. La parte opzioni internazionali e della lingua del pannello di controllo chiama anche **EnumSystemLocalesEx** per compilare l'elenco delle impostazioni locali che Visualizza. Tuttavia, per impostazione predefinita, le quattro pseudo-impostazioni locali elencate in precedenza non vengono riconosciute dal sistema, pertanto non verranno restituite da **EnumSystemLocalesEx**. Per i sistemi di Windows Vista fino a Windows 10, versione 1709, la soluzione consiste nell'abilitare le pseudo-impostazioni locali aggiungendo chiavi al registro di sistema di Windows.

Le modifiche vengono apportate sotto la \_ \_ \\ \\ chiave NLS del controllo CurrentControlSet di HKEY Local Machine System \\ \\ per le lingue installate nel sistema operativo. È possibile impostare queste impostazioni per abilitare le pseudo-impostazioni locali. Ogni chiave mostrata di seguito è l'LCID esadecimale corrispondente alle pseudo-impostazioni locali che vengono abilitate. Ogni valore è di tipo stringa (REG \_ SZ).

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

Per Windows 10, versione 1803, la modifica del registro di sistema di Windows come questa non ha alcun effetto. Tuttavia, è comunque possibile chiamare le API NLS non di enumerazione con i nomi delle pseudo-impostazioni locali (vedere gli esempi di codice precedenti) per popolare l'interfaccia utente (UI).

## <a name="related-topics"></a>Argomenti correlati

* [Uso del supporto per le lingue nazionali](using-national-language-support.md)
* [Pseudo-impostazioni locali](pseudo-locales.md)
* [EnumSystemLocalesEx](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [GetLocaleInfoEx](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [LocaleNameToLCID](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
