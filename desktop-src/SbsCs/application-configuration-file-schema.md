---
description: Di seguito è riportato l'elenco completo dello schema del file di configurazione dell'applicazione.
ms.assetid: c673dbff-cb64-4e90-88a8-c5f2c259f1d3
title: Schema del file di configurazione dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b05f1444e9a652d3cd20f5cefa2ac314bfe17868f47e4f34f6b485e42d4a41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142554"
---
# <a name="application-configuration-file-schema"></a>Schema del file di configurazione dell'applicazione

Di seguito è riportato l'elenco completo dello schema del file di configurazione dell'applicazione.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<Schema name="Microsoft per Application Configuration Schema" xmlns="urn:schemas-microsoft-com:xml-data"
                        xmlns:dt="urn:schemas-microsoft-com:datatypes">  
<!-- Attributes -->
<AttributeType name="manifestVersion" dt:type="enumeration" dt:values="1.0"/> 
<AttributeType name="name" dt:type="string"/>
<AttributeType name="type" dt:type="enumeration" dt:values="win32" required="yes"/>
<AttributeType name="publicKeyToken" dt:type="bin.hex"/>
<AttributeType name="language" dt:type="string"/>
<AttributeType name="processorArchitecture" dt:type="string"/>
<AttributeType name="version" dt:type="string"/>
<AttributeType name="oldVersion" dt:type="string"/>
<AttributeType name="newVersion" dt:type="string"/>
 
<!-- Elements-->
<ElementType name="configuration" model = "closed" content="eltOnly">
      <element type ="windows" minOccurs="0" maxOccurs="1"/>
</ElementType>
<ElementType name="windows" content="eltOnly">
      <element type="assemblyBinding" minOccurs="0" maxOccurs="1"/>
</ElementType>
<ElementType name="assemblyBinding" content="eltOnly">
      <element type="assemblyIdentity" minOccurs="1" maxOccurs="1"/>
      <element type="dependentAssembly" minOccurs="0" maxOccurs="*"/>
</ElementType>
<ElementType name="assemblyIdentity" model = "closed">
      <attribute type="type"  required="yes"/>
      <attribute type="name" required="yes"/>
      <attribute type="publicKeyToken" required="no"/>
      <attribute type="language" required="no"/>
      <attribute type="processorArchitecture"  required="yes" />
      <attribute type="version" required="no"/>
</ElementType>
<ElementType name="dependentAssembly"  model = "closed" content="eltOnly">
      <element type="assemblyIdentity" minOccurs="1" maxOccurs="1"/>
      <element type="bindingRedirect" minOccurs="1" maxOccurs="1"/>
</ElementType>
<ElementType name="bindingRedirect"  model = "closed">
      <attribute type="oldVersion" required="yes"/>
      <attribute type="newVersion" required="yes"/>
</ElementType>
</Schema>
```

 

 



