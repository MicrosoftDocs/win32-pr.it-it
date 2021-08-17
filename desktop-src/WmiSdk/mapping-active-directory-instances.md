---
description: In generale, ogni oggetto Active Directory esegue il mapping esattamente a un'istanza WMI.
ms.assetid: c6c7f3c3-7174-4278-bf40-d99ed8bd0c8d
ms.tgt_platform: multiple
title: Mapping delle istanze di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a3e40a6f4a85ebb1bb3d7e1e5a5de7bc43c754ff7672f694aff05b62853dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317638"
---
# <a name="mapping-active-directory-instances"></a>Mapping delle istanze di Active Directory

In generale, ogni oggetto Active Directory esegue il mapping esattamente a un'istanza WMI. La classe WMI corrispondente all'istanza WMI è uguale alla classe fornita dal provider di classi dalla classe Active Directory corrispondente. La proprietà chiave **ADSIPath di** ogni istanza viene compilata con il percorso ADSI dell'oggetto .

In questo argomento vengono illustrate le sezioni seguenti:

-   [Mapping degli spazi dei nomi](#mapping-namespaces)
-   [Mapping dei valori degli attributi](#mapping-attribute-values)
-   [Mapping delle associazioni di istanze](#mapping-instance-associations)

> [!Note]  
> Per altre informazioni sul supporto e sull'installazione di questo componente in un sistema operativo specifico, vedere Disponibilità del sistema [operativo dei componenti WMI.](operating-system-availability-of-wmi-components.md)

 

## <a name="mapping-namespaces"></a>Mapping degli spazi dei nomi

Ognuno degli spazi dei nomi in ADSI esegue il mapping uno-a-uno agli spazi dei nomi nello spazio dei nomi della \\ \\ directory radice WMI. Il nome dello spazio dei nomi WMI corrisponde al valore **ProgId** del provider di Servizi directory che fornisce lo spazio dei nomi. In particolare, Active Directory esegue il mapping allo \\ spazio dei nomi LDAP nello spazio dei nomi della directory \\ \\ radice. WMI crea lo \\ spazio dei nomi LDAP come parte del processo di registrazione del provider di classi.

## <a name="mapping-attribute-values"></a>Mapping dei valori degli attributi

Nella tabella seguente viene elencato il mapping tra ogni attributo di un oggetto di Active Directory e una proprietà WMI.



| Sintassi di Active Directory | Tipo di dati WMI                                 | Valore della proprietà WMI                                                        |
|-------------------------|-----------------------------------------------|---------------------------------------------------------------------------|
| Access-Point            | **STRINGA \_ CIM**                               | Mappato dal valore della stringa.                                      |
| Boolean                 | **CIM \_ BOOLEAN**                              | Mappato direttamente al valore booleano appropriato.                         |
| Stringa senza distinzione tra maiuscole e minuscole | **STRINGA \_ CIM**                               | Mappato dal valore della stringa.                                      |
| Stringa con distinzione tra maiuscole e minuscole   | **STRINGA \_ CIM**                               | Mappato dal valore della stringa.                                      |
| Nome distinto      | **STRINGA \_ CIM**                               | Mappato dal valore della stringa.                                      |
| DN-Binary               | Oggetto incorporato della classe **DN \_ con \_ binario** | Mappato a istanze della **classe DN \_ With \_ String.**                    |
| DN-String               | Oggetto incorporato della classe **DN \_ con \_ stringa** | Mappato a istanze della **classe DN \_ With \_ String.**                    |
| Enumerazione             | **CIM \_ SINT32**                               | Mappato direttamente al valore intero.                                     |
| IA5-String              | **STRINGA \_ CIM**                               | Mappato dal valore della stringa.                                      |
| Intero                 | **CIM \_ SINT32**                               | Mappato direttamente al valore intero.                                     |
| Descrittore di sicurezza NT  | Oggetto incorporato della classe **Uint8Array**       | Mappato a istanze della **classe Uint8Array.**                          |
| Stringa numerica          | **STRINGA \_ CIM**                               | Mappato dal valore della stringa.                                      |
| ID oggetto               | **STRINGA \_ CIM**                               | Mappato dalla rappresentazione di stringa dell'OID; ad esempio "1.3.3.4". |
| Octet String            | Oggetto incorporato della classe **Uint8Array**       | Mappato a istanze della **classe Uint8Array.**                          |
| OR Name                 | **STRINGA \_ CIM**                               | Mappato dal valore della stringa.                                      |
| Presentation-Address    | **STRINGA \_ CIM**                               | Mappato dal valore della stringa.                                      |
| Stampa stringa maiuscole/minuscole       | **STRINGA \_ CIM**                               | Mappato dal valore della stringa.                                      |
| Collegamento di replica            | Oggetto incorporato della classe **Uint8Array**       | Mappato a istanze della **classe Uint8Array.**                          |
| SID                     | Oggetto incorporato della classe **Uint8Array**       | Mappato a istanze della **classe Uint8Array.**                          |
| Ora                    | **CIM \_ DATETIME**                             | Convertito nella rappresentazione \_ CIM DATETIME ed eseguito il mapping.                 |
| Non definito               | N/D                                           | N/D                                                                       |
| Stringa Unicode          | **STRINGA \_ CIM**                               | Mappato dal valore della stringa.                                      |
| Ora UTC codificata          | **CIM \_ DATETIME**                             | Convertito nella rappresentazione \_ CIM DATETIME ed eseguito il mapping.                 |



 

Per altre informazioni su **Uint8Array** e **DN \_ with \_ Binary,** vedere [Mapping Attributes](mapping-active-directory-classes.md).

## <a name="mapping-instance-associations"></a>Mapping delle associazioni di istanze

Il provider di Servizi directory esegue il mapping delle diverse relazioni tra contenitori in Active Directory usando istanze della classe di contenimento dell'istanza [**\_ LDAP \_ \_ DS.**](/previous-versions/windows/desktop/dsprov/ds-ldap-instance-containment)

 

 
