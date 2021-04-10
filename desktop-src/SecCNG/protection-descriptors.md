---
description: Una stringa di regola del descrittore di protezione contiene un elenco sequenziale di una o più protezioni.
ms.assetid: FBFE2143-DC40-40F3-83CE-E6D8841F9C11
title: Descrittori di protezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11814df2af5bd9abee4260f4aadab5bb74c77a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227050"
---
# <a name="protection-descriptors"></a>Descrittori di protezione

Una stringa di regola del descrittore di protezione contiene un elenco sequenziale di una o più protezioni. Deve essere presente almeno una protezione. Se è presente più di un oggetto, le protezioni devono essere separate nella stringa tramite **and** o **or**. Questi valori devono essere in lettere maiuscole. Nella sintassi seguente viene illustrato il formato stringa di un descrittore di protezione.


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



È attualmente possibile definire i descrittori di protezione per i seguenti tipi di autorizzazione:

-   Gruppo in una foresta Active Directory.
-   Un set di credenziali Web.
-   Un certificato nell'archivio certificati dell'utente.

Di seguito sono riportati alcuni esempi di stringhe di regole per i descrittori di protezione per un gruppo Active Directory:

-   "SID = S-1-5-21-4392301 E SID = S-1-5-21-3101812"
-   "SDDL = O:S-1-5-5-0-290724G: SYD: (A;; CCDC;;; S-1-5-5-0-290724) (A;;D C;;; WD) "
-   "LOCAL = User"
-   "LOCAL = computer"

Di seguito sono riportati alcuni esempi di stringhe di regole descrittore di protezione per un set di credenziali Web:

-   "Webcredentials = Passwordname"
-   "Webcredentials = filepasswordname, WebPersonale. com"

Di seguito sono riportati alcuni esempi di stringhe di regole descrittore di protezione per un certificato:

-   "CERTIFICAte = HashID: \_ hash SHA1 \_ del \_ certificato"
-   "CERTIFICAte = CertBlob: base64String"

Il descrittore di protezione specificato determina automaticamente il provider di protezione con chiave. Per ulteriori informazioni, vedere [provider di protezione](protection-providers.md).

Si noti che il lato sinistro del segno di uguale (=) deve essere **SID**, **SDDL**, **local**, **webcredentials** o **Certificate**. I valori non fanno distinzione tra maiuscole e minuscole.

Quando si chiama la funzione [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) , è necessario specificare una stringa di regola (o un nome visualizzato associato a una stringa di regola). In alternativa, poiché le stringhe delle regole del descrittore di protezione sono piuttosto complesse da usare e ricordare, è possibile associare un nome visualizzato alla stringa della regola e registrarsi entrambi usando la funzione [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) . Quindi, è possibile usare il nome visualizzato in **NCryptCreateProtectionDescriptor**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DPAPI CNG](cng-dpapi.md)
</dt> <dt>

[Provider di protezione](protection-providers.md)
</dt> </dl>

 

 



