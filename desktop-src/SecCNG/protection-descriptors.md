---
description: Una stringa della regola del descrittore di protezione contiene un elenco sequenziale di una o più protezioni.
ms.assetid: FBFE2143-DC40-40F3-83CE-E6D8841F9C11
title: Descrittori di protezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e99d4ec8de08ad2f657d2b3ac1992ce6e399ede277f8fde3e12f0732571b01a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907253"
---
# <a name="protection-descriptors"></a>Descrittori di protezione

Una stringa della regola del descrittore di protezione contiene un elenco sequenziale di una o più protezioni. Deve essere presente almeno una protezione. Se sono presenti più di uno, le protezione devono essere separate nella stringa da **AND** o **OR**. Questi valori devono essere in maiuscolo. La sintassi seguente illustra il formato stringa di un descrittore di protezione.


```C++
Descriptor = [ Protector-or
              *( OR-separator Protector-or ) ]

    Protector-or = Protector-and
              *( AND-separator Protector-and )

    OR-separator = "OR"
    AND-separator = "AND"

    Protector-and = providerName EQUALS providerAttributes

    providerName = descr

    providerAttribute = string | hexstring

      ; The following characters are to be escaped when they appear
      ; in the value to be encoded: ESC, one of <escaped>, leading
      ; SHARP or SPACE, trailing SPACE, and NULL.
      string =   [ ( leadchar / pair ) [ *( stringchar / pair )
         ( trailchar / pair ) ] ]

      leadchar = LUTF1 / UTFMB
      LUTF1 = %x01-1F / %x21 / %x24-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      trailchar  = TUTF1 / UTFMB
      TUTF1 = %x01-1F / %x21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      stringchar = SUTF1 / UTFMB
      SUTF1 = %x01-21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      pair = ESC ( ESC / special / hexpair )
      special = escaped / SPACE / SHARP / EQUALS
      escaped = DQUOTE / PLUS / COMMA / SEMI / LANGLE / RANGLE
      hexstring = SHARP 1*hexpair
      hexpair = HEX HEX

      descr   = leadkeychar *keychar
      leadkeychar = ALPHA
      keychar = ALPHA / DIGIT / HYPHEN
      number  = DIGIT / ( LDIGIT 1*DIGIT )

      ALPHA   = %x41-5A / %x61-7A   ; "A"-"Z" / "a"-"z"
      DIGIT   = %x30 / LDIGIT       ; "0"-"9"
      LDIGIT  = %x31-39             ; "1"-"9"
      HEX     = DIGIT / %x41-46 / %x61-66 ; "0"-"9" / "A"-"F" / "a"-"f"

      NULL    = %x00 ; null (0)
      SPACE   = %x20 ; space (" ")
      DQUOTE  = %x22 ; quote (""")
      SHARP   = %x23 ; octothorpe (or sharp sign) ("#")
      DOLLAR  = %x24 ; dollar sign ("$")
      SQUOTE  = %x27 ; single quote ("'")
      LPAREN  = %x28 ; left paren ("(")
      RPAREN  = %x29 ; right paren (")")
      PLUS    = %x2B ; plus sign ("+")
      COMMA   = %x2C ; comma (",")
      HYPHEN  = %x2D ; hyphen ("-")
      DOT     = %x2E ; period (".")
      SEMI    = %x3B ; semicolon (";")
      LANGLE  = %x3C ; left angle bracket ("<")
      EQUALS  = %x3D ; equals sign ("=")
      RANGLE  = %x3E ; right angle bracket (">")
      ESC     = %x5C ; backslash ("\")
      USCORE  = %x5F ; underscore ("_")
      LCURLY  = %x7B ; left curly brace "{"
      RCURLY  = %x7D ; right curly brace "}"

      ; Any UTF-8 [RFC3629] encoded Unicode [Unicode] character
      UTF8    = UTF1 / UTFMB
      UTFMB   = UTF2 / UTF3 / UTF4
      UTF0    = %x80-BF
      UTF1    = %x00-7F
      UTF2    = %xC2-DF UTF0
      UTF3    = %xE0 %xA0-BF UTF0 / %xE1-EC 2(UTF0) /
                %xED %x80-9F UTF0 / %xEE-EF 2(UTF0)
      UTF4    = %xF0 %x90-BF 2(UTF0) / %xF1-F3 3(UTF0) /
                %xF4 %x80-8F 2(UTF0)

      OCTET   = %x00-FF ; Any octet (8-bit data unit)
```



I descrittori di protezione possono attualmente essere definiti per i tipi di autorizzazione seguenti:

-   Gruppo in una foresta Active Directory.
-   Set di credenziali Web.
-   Certificato nell'archivio certificati dell'utente.

Di seguito sono riportati alcuni esempi di stringhe di regole del descrittore di protezione per un gruppo di Active Directory:

-   "SID=S-1-5-21-4392301 E SID=S-1-5-21-3101812"
-   "SDDL=O:S-1-5-5-0-290724G:SYD:(A;; CCDC;; S-1-5-5-0-290724)(A;;D C;;; WD)"
-   "LOCAL=user"
-   "LOCAL=machine"

Di seguito sono riportati alcuni esempi di stringhe di regole del descrittore di protezione per un set di credenziali Web:

-   "WEBCREDENTIALS=MyPasswordName"
-   "WEBCREDENTIALS=MyPasswordName,myweb.com"

Di seguito sono riportati alcuni esempi di stringhe di regole del descrittore di protezione per un certificato:

-   "CERTIFICATE=HashID:sha1 \_ hash \_ del \_ certificato"
-   "CERTIFICATE=CertBlob:base64String"

Il descrittore di protezione specificato determina automaticamente quale provider di protezione delle chiavi viene usato. Per altre informazioni, vedere [Provider di protezione](protection-providers.md).

Si noti che il lato sinistro del segno di uguale (=) deve essere **SID,** **SDDL,** **LOCAL,** **WEBCREDENTIALS** o **CERTIFICATE.** I valori non fanno distinzione tra maiuscole e minuscole.

È necessario specificare una stringa di regola (o un nome visualizzato associato a una stringa di regola) quando si chiama la [**funzione NCryptCreateProtectionDescriptor.**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) In alternativa, poiché le stringhe delle regole del descrittore di protezione sono piuttosto ingombranti da usare e ricordare, è possibile associare un nome visualizzato alla stringa della regola e registrarle entrambe usando la funzione [**NCryptRegisterProtectionDescriptorName.**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) È quindi possibile usare il nome visualizzato in **NCryptCreateProtectionDescriptor**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[Provider di protezione](protection-providers.md)
</dt> </dl>

 

 



